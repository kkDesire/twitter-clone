<template>
    <div class="flex flex-col">
        <!-- begin ::: Preview Card => What's happening ::: -->
        <SidebarRightPreviewCard title="What's happening">
            <!-- begin ::: items ::: -->
            <SidebarRightPreviewCardItem v-for="whatsHappening in whatsHappeningItems">
                <!-- begin ::: item content ::: -->
                <div>
                    <!-- begin ::: title ::: -->
                    <h2 class="font-bold text-gray-800 dark:text-white">{{ whatsHappening.title }}</h2>
                    <!-- end ::: title ::: -->
                    <!-- begin ::: count ::: -->
                    <p class="text-xs text-gray-400">{{ whatsHappening.count }}</p>
                    <!-- begendin ::: count ::: -->
                </div>
                <!-- end ::: item content ::: -->
            </SidebarRightPreviewCardItem>
            <!-- end ::: items ::: -->
        </SidebarRightPreviewCard>
        <!-- end ::: Preview Card => What's happening ::: -->

        <!-- begin ::: Preview Card => Who to  follow ::: -->
        <SidebarRightPreviewCard title="Who to  follow">
            <!-- begin ::: items ::: -->
            <SidebarRightPreviewCardItem v-for="whoToFollow in whoToFollowItems">
                <!-- begin ::: item content ::: -->
                <div class="flex flex-row justify-between p-2">
                    
                    <!-- begin ::: picture and name/username ::: -->
                    <div class="flex flex-row items-center">
                        <!-- begin ::: picture ::: -->
                        <img
                            :src="whoToFollow.image"
                            class="w-10 h-10 rounded-full"
                            :alt="whoToFollow.name"
                        >
                        <!-- end ::: picture ::: -->

                        <!-- begin ::: name/username ::: -->
                        <div class="flex flex-col ml-2">
                            <!-- begin ::: name ::: -->
                            <h1 class="text-sm font-bold text-gray-900 dark:text-white">{{ whoToFollow.name }}</h1>
                            <!-- end ::: name ::: -->

                            <!-- begin ::: username ::: -->
                            <p class="text-xs text-gray-400">{{ whoToFollow.username }}</p>
                            <!-- begendin ::: username ::: -->
                        </div>
                        <!-- end ::: name/username ::: -->
                    </div>
                    <!-- end ::: picture and name/username ::: -->

                    <!-- begin ::: follow button ::: -->
                    <div class="flex  h-full">
                        <button class="bg-black font-bold text-white p-2 px-4 rounded-full dark:bg-white dark:text-black">Follow</button>
                    </div>
                    <!-- begendin ::: follow button ::: -->
                </div>
                <!-- end ::: item content ::: -->
                <!-- begin ::: items ::: -->
            </SidebarRightPreviewCardItem>
            <!-- end ::: items ::: -->
        </SidebarRightPreviewCard>
        <!-- end ::: Preview Card =>Who to  follow ::: -->
    </div>
</template>

<script lang="ts" setup>

const whatsHappeningItems = ref([
    {
        title: 'spaceX',
        count: '18.8K Tweets',
    },
    {
        title: 'spaceX',
        count: '18.8K Tweets',
    },
    {
        title: 'spaceX',
        count: '18.8K Tweets',
    }
])

const whoToFollowItems = ref([
    {
        name: 'John Doe',
        username: '@johnDoe',
        image: 'https://picsum.photos/200/200',
    },
    {
        name: 'Désiré Kouassi',
        username: '@desireKouassi',
        image: 'https://picsum.photos/200/200',
    },
    {
        name: 'Auguinard Kouamé',
        username: '@auguinardKouame',
        image: 'https://picsum.photos/200/200',
    }
])
</script>

