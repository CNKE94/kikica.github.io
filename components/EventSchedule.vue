<script setup lang="ts">
const details = [{
    heading: "Црквено Венчање",
    icon: "church.svg",
    time: "13:30 часова",
    place: "Црква Св пророка Илије",
    address: "Витезова Карађорђеве звезде 61, 11160 Миријево"
}, {
    heading: "Ресторан",
    icon: "restaurant.svg",
    time: "16:00 часова",
    place: "Ресторан Филмски Град",
    address: "Кнеза Вишеслава 88, 11090 Београд"
}, {
    heading: "Грађанско Венчање",
    icon: "wedding.svg",
    time: "17:15 часова",
    place: "Ресторан Филмски Град",
    address: "Кнеза Вишеслава 88, 11090 Београд"
}
];
</script>

<template>
    <AppContainer class="flex flex-col bg-orange-200">
        <div class="text-center pb-10 mb-10 border-b-2 border-orange-500">
            <p>Распоред догађаја</p>
            <AppHeading class="text-3xl mt-3" heading="h2" title="Недеља, 22. Октобар 2025"></AppHeading>
        </div>
        <div class="grid gap-5 sm:grid-cols-1 lg:grid-cols-2">
            <AppCard
             v-for="(event, index) in details"
             :key="index"
             :heading="event.heading" 
             :icon="`/images/${event.icon}`"
             :time="event.time" 
             :place="event.place"
             :address="event.address"
            />
        </div>
    </AppContainer>
</template>