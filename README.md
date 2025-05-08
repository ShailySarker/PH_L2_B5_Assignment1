# Blog Task

**What is the use of the keyof keyword in TypeScript? Provide an example.**

```ts

In TypeScript, the keyof keyword is used as a type operator. It helps access each property of an object type. It ensures type safety and prevents unwanted access to properties that do not exist.


Example:

type Person = {
    name: string;
    age: number;
    address: string;
}

type PersonInfo = keyof Person;

const person1: PersonInfo = "name";
const person2: PersonInfo = "age";
const person3: PersonInfo = "address";

```

**Provide an example of using union and intersection types in TypeScript.**

```ts


**Union type(|):** It combines multiple types into one, allowing a value to be any one of them.

Example:

type Developer = "Junior Developer" | "Senior Developer" | "Pro Developer";

const newDeveloper: Developer = "Junior Developer";


**Intersection type(&):** It Combines multiple types into one, requiring a value to satisfy all of them.

Example:

type FrontendDeveloper = {
    skills: string[];
    designation1: "Frontend Developer"
};
type BackendDeveloper = {
    skills: string[];
    designation2: "Backend Developer"
};

type FullStackDeveloper = FrontendDeveloper & BackendDeveloper;

const fullStackDeveloper: FullStackDeveloper = {
    skills: ["HTML", "CSS", "ReactJS", "NextJS", "Redux" "ExpressJS", "NodeJS", "MongoDB", "Mongoose"],
    designation1: "Frontend Developer",
    designation2: "Backend Developer"
};


```
