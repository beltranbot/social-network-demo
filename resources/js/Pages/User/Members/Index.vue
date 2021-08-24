<template>
    <pages-layout>
        <template #title>
            <div class="flex flex-col items-center sm:flex-row sm:justify-between">
                <h2 class="flex items-end font-semibold text-xl text-gray-800 leading-tight">
                    <Link :href="route('members.index')" class="capitalize underline">
                        Members
                    </Link>
                </h2>
                <span class="text-gray-800 leading-tight text-lg capitalize mt-5 sm:mt-0">
                    Visit your
                    <Link href="#" class="underline hover:text-green-500">friends</Link>
                </span>
            </div>
        </template>
        <UserBlock :items="members"></UserBlock>
    </pages-layout>
</template>

<script>
import PagesLayout from '@/Layouts/PagesLayout.vue'
import { Link } from '@inertiajs/inertia-vue3';
import UserBlock from "@/Components/UserBlock";
export default {
    props: ["members"],
    components: {
        PagesLayout,
        Link,
        UserBlock
    }
}
</script>
