<script setup lang="ts">
import {inject, reactive} from "vue";
import {RouterLink} from "vue-router";
import type {Member} from "@/interfaces";

const memberList = inject("memberList") as Map<number, Member>;
const member: Member = reactive(
    {
        id:0,
        name: "",
        email: "",
        points: 0,
        note: ""
    }
);
const onAdd = (): void => {
    console.log(member);
};
</script>


<template>
    <h1>会員管理</h1>
    <nav id="breadcrumbs">
        <ul>
            <li>
                <RouterLink v-bind:to="{name: 'AppTop'}">
                TOP
                </RouterLink>
            </li>
            <li>
            <RouterLink v-bind:to="{name: 'MemberList'}">
            会員リスト
            </RouterLink>
            </li>
            <li>会員詳細情報</li>
            <li>会員情報追加</li>
        </ul>
    </nav>
</template>