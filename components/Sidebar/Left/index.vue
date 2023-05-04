<template>
    <div class="flex flex-col h-screen">
        <!-- begin ::: Twitter icon ::: -->
        <div
                class="p-2 my-2 hover:bg-blue-50 rounded-full w-min dark:hover:bg-white/20"
                :class="defaultTransition"
        >
            <nuxt-link to="/">
                <div class="w-8 h-8">
                    <LogoTwitter/>
                </div>
            </nuxt-link>
        </div>
        <!-- end ::: Twitter icon ::: -->

        <!-- begin ::: sidebar content ::: -->
        <div class="mt-2 space-y-3">
            <!-- begin ::: Home ::: -->
            <SidebarLeftTab active>
                <template #icon>
                    <HomeIcon/>
                </template>
                <template #name>Home</template>
            </SidebarLeftTab>
            <!-- end ::: Home ::: -->

            <!-- begin ::: Explore ::: -->
            <SidebarLeftTab>
                <template #icon>
                    <HashtagIcon/>
                </template>
                <template #name>Explore</template>
            </SidebarLeftTab>
            <!-- end ::: Explore ::: -->

            <!-- begin ::: Notification ::: -->
            <SidebarLeftTab>
                <template #icon>
                    <BellIcon/>
                </template>
                <template #name>Notification</template>
            </SidebarLeftTab>
            <!-- end ::: Notification ::: -->

            <!-- begin ::: Messages ::: -->
            <SidebarLeftTab>
                <template #icon>
                    <InboxIcon/>
                </template>
                <template #name>Messages</template>
            </SidebarLeftTab>
            <!-- end ::: Messages ::: -->

            <!-- begin ::: Bookmarks ::: -->
            <SidebarLeftTab>
                <template #icon>
                    <BookmarkIcon/>
                </template>
                <template #name>Bookmarks</template>
            </SidebarLeftTab>
            <!-- end ::: Bookmarks ::: -->

            <!-- begin ::: Lists ::: -->
            <SidebarLeftTab>
                <template #icon>
                    <DocumentTextIcon/>
                </template>
                <template #name>Lists</template>
            </SidebarLeftTab>
            <!-- end ::: Lists ::: -->

            <!-- begin ::: Profile ::: -->
            <SidebarLeftTab>
                <template #icon>
                    <UserIcon/>
                </template>
                <template #name>Profile</template>
            </SidebarLeftTab>
            <!-- end ::: Profile ::: -->

            <!-- begin ::: More ::: -->
            <SidebarLeftTab>
                <template #icon>
                    <EllipsisHorizontalCircleIcon/>
                </template>
                <template #name>More</template>
            </SidebarLeftTab>
            <!-- end ::: More ::: -->
        </div>
        <!-- end ::: sidebar content ::: -->
    </div>
</template>

<script setup>
import { HomeIcon } from "@heroicons/vue/20/solid";
import { HashtagIcon, BellIcon, InboxIcon, BookmarkIcon, DocumentTextIcon, UserIcon, EllipsisHorizontalCircleIcon } from "@heroicons/vue/24/outline";

const {defaultTransition} = useTailwindConfig();
</script>