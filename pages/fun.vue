<template>
    <div>
        <h1>Fun Page</h1>
        <NuxtLink to="/">Home page</NuxtLink>
    </div>
</template>
<script setup lang="ts">

type User = {
    readonly _id: string,
    name: string
    age: number
    isActive: boolean
    cardDetails?: number
}

function createUser(user: User): User {
    return {_id: user._id, name: user.name, age: user.age, isActive: user.isActive};
}

let firstUser = createUser({_id: "1234", name: "Aki", age: 33, isActive: true});

let secondUser: User = {
    _id: "1234",
    name: "bob",
    age: 33,
    isActive: true,
    cardDetails: 1234
}

type cardNumber = {
    cardnumber: number
}

type cardDate = {
    carddate: string
}

type cardDetails = cardNumber & cardDate & {
    cvc: number
}

let card: cardDetails = {
    cardnumber: 234,
    carddate: "hello",
    cvc: 123
}

const arr: string[] = [];
arr.push("helo");

const arrPower: Array<number> = [];
arrPower.push(3);

const arrUsers: User[] = [];
arrUsers.push({_id: "1234", name: "Aki", age: 33, isActive: true});
arrUsers.push({_id: "34", name: "ghki", age: 73, isActive: false});

const arrCards: cardDetails[] = [];
arrCards.push({
    cardnumber: 234,
    carddate: "hello",
    cvc: 123
});

const arrOfArr: number[][] = [];
arrOfArr.push(
    [4, 5, 6],
    [5, 6, 7, 9]
)

type Guest = {
    name: string,
    id: number
}

type Admin = {
    nick: string,
    age: number
}

let guy: Guest | Admin = {name: "boy", id: 33}

let getId = (id: number | string) => {
    return `Id is ${id}`
}

getId(4);
getId("5");

console.log("Hellow World!", getId(55));

</script>