## Name

Antonio Gonzalez Fernandez (a.k.a. Jorin)

## Project name

#### Shiken 
(from "試験" [しけん, shiken], exam in Japanese)

## Members Github handlers

Only me, @iam-agf

## Links

[Twitter](https://twitter.com/cosmo_jorin)

[Github](https://github.com/iam-agf)


## Title for the grant request

Shiken 

## Grant type

Tinker

## Description

Given the [issue about hiring processes](https://github.com/gnolang/hackerspace/issues/13) I had this idea of contributing adding tools for evaluating candidates and students via a realm that could produce exams/tests for this purpose. 

The main goal of this realm is to be used as a tool for the mentioned issue, but also can be used for others to create their own exams for the purpose they find useful.

So this questions realm would have the following types of questions: 

- **True-False** options (the creator of the question only inputs the answer as True or False and the candidate would have to decide)
- **Multiple** options (the creator of the question adds different options and the candidate would have to choose)
- **Open ended** (the creator lets the candidate answer openly)

The owner will be able to create, query and edit `questions`. These questions would be stored in a `repository` where the owner will be able to add, edit or delete questions, register/remove editors for a created exam (addresses that will be able do the same actions on questions except deleting), or transfer ownership of the whole repository. Finally the editors (it's implicit the owner is included in this group) of the `repository` will be able to create `exams`. They would be able to edit the availability time/block heights to visualize the exam for the registered address(es), and other tools. Finally a last part would be a component in the realms to  for applicants.

## Goals

The idea is to create three packages: `Questions`, `Exams`, `Repositories`, and a website with several components to manipulate a realm that will hold a repository where the user will be able to:
* Query the questions & exams stored in this repository.
* Solve exams.
* Have a smoother control of all the functions related to the repository.

Below I provide an attempt of the project model.*

\* The exposed functions and structures given here may not be the final ones. They could be edited during the release to give a better product.


####`Questions` 
(currently 1 struct, 7 functions)


```go
type Question struct {
    questionType uint
    tags avl.Tree
    content string
    answer string
    options []string
}
```

```go
func NewQuestion

func UpdateContent
func UpdateTags
func UpdateOptions
func UpdateAnswer

func GetAnswer // This will return an offchain encrypted answer the author would require to decrypt offchain too. That's the reason of the website
func GetContent 
func GetOptions

```

#### `Exams` 
(currently 1 struct, 16 functions)
```go
type Exam struct {
    creator std.Address
    title string
    description string
    questions []Question
    ponderation avl. Tree // Some questions could have more value than others.
    applicants avl.Tree
    tags avl.Tree
    times avl.Tree
    responsesApplicants avl.Tree
    record []string
}
```

```go

func GetTitle
func UpdateTitle

func GetDescription
func UpdateDescription

func NewQuestion
func GetQuestions
func RemoveQuestion
// In this case editQuestion is done at repository level, not exam

func NewApplicant
func RemoveApplicant
func GetApplicants
// EditApplicant is equivalent to delete an address and add a new one, so can be done in a safer way with removal and add.


func SendResponse // Will overwrite the previous answer of an applicant.
func GetResponses
func GetResponse

func AddTimes
func UpdateTimes

func getRecord // Will return all the edits from editors and owner since creation of exam
```

#### `Repositories`
(currently 1 struct, 17 functions)

```go
type Repository struct {
    owner std.Address
    questions []Question
    tags avl.Tree
    editors avl.Tree
    exams avl.Tree
    record []string
}
```

```go
func NewRepository

func transferOwnership

func NewQuestion // Add a question to this repository
func GetQuestion // Question by id
func GetQuestions // List of questions
func RemoveQuestion
func EditQuestion

func NewTag // Tags can exist without a question with it
func GetTags
func DeleteTag

func GetEditors
func RemoveEditor

func NewExam
func GetExam
func GetExamsByTag
func RemoveExam
func EditExamTitle

func getRecord // Will return all the edits from editors and owner since creation of exam


```

It's necessary to state clear that the main reason of using a website instead of using a rendering of the realms is because would **allow to encrypt the answers of the questions via an owner password** through a external function in the website.

The process to encrypting would be the following:

1. Examinator enters the website tab to make a new exam.
2. This will generate a key pair `(pub, priv)`. 
3. If the examinator sends an exam on chain, he will receive the key `priv` generated so will have to store/save it. 
4. The `pub` key will be sent on the tx as part of the message.

In the case of the applicants they don't require to do anything more than answering the exam since the login would be

1. They enter the exam because they have an allowed address
2. When they call the exam:
2.1. The browser will receive the key `pub` stored along with the exam.
2.2. The browser will generate a symmetric key `sym`.
3. When they send their answer, it will be encrypted with the `sym` key and
4. The `pub` key generated will encrypt the symmetric key `sym`.
5. Both encrypted messages, `symmetricEncrypted(answer)` and `asymmetricEncrypted(sym)` will be sent as part of their tx.

Because of this, when the evaluator calls for the answer, the browser will first decrypt the symmetric key `sym`, and then will use it decrypt the answer. This way there is no way the applicants can copy each other. Another thing to mention is that the exam won't be seen identical by the applicants since the questions will be disordered so the answers and the encrypting will be almost impossible to be identical. For more information about the encrypting process [please check this dummy model created to briefly explain how it would work](https://github.com/iam-agf/encryptModel) and don't hesitate asking me any detail on the vision and work flow I have about this project.

## Contributions, issues and pull requests made to Gno and Game of Realms 

None related to GNO. Only [one in ignite/cli](https://github.com/ignite/cli/pull/3564) , but still not merged.

## Why are you best suited/what is your background?

As a developer I have 4 years of experience, I have been involved in crypto since last year, have knowledge in many languages like python, dart, javascript, go; I have participated in web3-based events like the [hackatom of 2022](https://github.com/EmpowerPlastic/Hackatom_2022) aand now I believe I can deliver valuable content to GNO starting with this idea.

## Milestones and overall time frame of your proposal

Splitting the parts of the project into smaller ones, These are my estimations for each part:

|Id | Activity | Expected | Worse scenario |
|:-:|----------|:-:|:-:|
| | **First repository** |
| 1 | Package `Questions` | 2 | 3 |
| 2 | Package `Repositories` | 2 | 3 |
| 3 | Package `Exams` | 3 | 5 |
| 4 | Realm for interacting repositories, questions and exams | 2 | 4 |
| 5 | Realm to render repositories data like questions and exams | 2 | 3 |
|  | **First Total** | **11** | **18** |
| | **Second repository** |
| 6 | Website view for repository visualising (questions & exams) | 2 | 3 |
| 8 | Website exam creation | 3 | 5 |
| 8 | Website exam application (only exams) | 3 | 4 |
| 9 | Documentation for all the previously mentioned components | 1 | 2 |
|  | **Second Total** | **9** | **14** |
|  | **Final Total** | **20** | **32** |
Meaning an approximate of 5 months, and in a (very) worst scenario 8 months.

The milestones can be understood as the deliver of each of the listed parts above. As a DAG, the graph for doing each section can be understood as this:

```    
┌───────────────┐                                                                                    
│P Questions (1)│                                                                                    
└┬──────────────┘                                                                                    
┌▽───────────────┐                                                                                   
│P Repository (2)│                                                                                   
└┬───────────────┘                                                                                   
┌▽───────────────────────────────────────────────────────────────────────┐                           
│P Exam (3)                                                              │                           
└┬──────────────────────────────────────────────────────────────────────┬┘                           
┌▽────────────────────────────────────────────────────────────────────┐┌▽──────────────────┐         
│Realm to Interact (4)                                                ││Realm to render (5)│         
└┬───────────────────────────────────┬───────────────────────────────┬┘└───────────────────┘         
┌▽─────────────────────────────────┐┌▽─────────────────────────────┐┌▽──────────────────────────────┐
│View exam application (8)         ││View repository manipulate (7)││View repository visualising (6)│
└┬─────────────────────────────────┘└┬─────────────────────────────┘└───────────────────────────────┘
┌▽───────────────────────────────────▽┐                                                              
│Documentation (9)                    │                                                              
└─────────────────────────────────────┘                                                              

```

Notes:

- Weeks are understood as working weeks, i.e. only from Monday to Friday. 
- The packages `Questions`, `Repositories` and `Exams` would be built separately and will be joint all to become only one. Firstly each part would be independent to work easier. If it's better to have a package per structure, it can be done that way.
- The realms renders would only  show the questions and exams since currently it's not possible to encrypt the answers of the questions via a password on chain since it would expose the password. 
- For the answers encryption would require an external tool in the website to encrypt the answers to send them to the chain for avoiding chances of copying. The method is explained in the goals. This is one of the heaviest and most relevant parts, so that's why I insist on it.

## Your idea for fair funding of the proposal

Based on the [salaries of a Go developer](https://www.google.com/search?client=safari&rls=en&q=junior+golang+salary&ie=UTF-8&oe=UTF-8), since my knowledge in Go is Junior~Mid, I consider it's approximate the upper range of a junior dev in that table (80,000 per year). This divided by [the amount of working hours in a year](https://www.google.com/search?client=safari&rls=en&q=working+hours+in+a+year&ie=UTF-8&oe=UTF-8) (2080), would be an average of 80,000/2080 ~38 USD per hour. So considering the previous table, I think the amount for the grant would be 

(hour rate) x (working hours in a week) x (weeks the project will take) =

38 x 40 x 20 = 30,400 USD


## What do you and the submission bring to the Gno.land platform and community?

#### Me 
As a developer I want to continue reaching new levels of Go knowledge and I think GNO is a good place where I can grow these skills. Also this can help me give meaningful contributions for the benefit of the chain knowing what is missing or required to make the code better for others.

#### The submission

The main goal of this project is to <u>**evaluate applicants to measure their skills**</u>.

But given the transparency of blockchain this tool can also 
* <u>**Provide applicants with lists of questions to applicants to prepare and study before applying to exams**</u> if the evaluators make their questions visible when adding questions to their repository and 
* <u>**Results will be transparent for both sides**</u>, making the exams honest, since the answers by candidates will be onchain for everyone and the private keys will require to be published onchain too after every exam.

As a collateral result, this project will 
* Provide <u>**a simple infrastructure for sending private messages between addresses**</u>

which can be useful for others after refining this part project. 

## Share any referrals or other projects you work with

[This is the only team with whom I have worked in 
web3](https://github.com/empowerchain)

If it's required I can share my linkedin to the interested part.
