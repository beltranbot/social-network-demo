<template>
    <aside class="flex flex-col bg-white shadow py-6 w-full sm:w-1/3 lg:w-1/4">
        <Link :href="route('profiles.show', $page.props.user.username)" class="flex items-end pl-6 py-2 text-gray-800 hover:bg-gray-500 hover:text-white">
            <img :alt="$page.props.user.username" :src="$page.props.user.profile_photo_url" class="h-8 w-8 rounded-full object-cover">
            <span class="ml-2">{{ $page.props.user.username }}</span>
        </Link>
    </aside>
</template>

<script>
import { Link } from '@inertiajs/inertia-vue3';
export default {
    components: {
        Link,
    }
}
</script>