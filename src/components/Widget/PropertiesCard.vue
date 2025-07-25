<script setup>
defineProps({
    data: { type: Object }
})
</script>
<template>
    <div class="properties-card">
        <div class="relative title-image">
            <BaseImage class="image-responsive" :image="data.image" alt="image" />
        </div>
        <div class="card-body">
            <BaseParagraph><i class="fa-solid fa-location-dot"></i> {{ data.location }}</BaseParagraph>
            <SubTitle>{{ data.title }}</SubTitle>
            <ul>
                <ListItem><i class="fa-solid fa-bed"></i> {{ data.bedrooms }} bed</ListItem>
                <ListItem><i class="fa-solid fa-bath"></i> {{ data.bathrooms }} bath</ListItem>
                <ListItem><i class="fa-solid fa-maximize"></i> {{ area }} sqft</ListItem>
            </ul>
            <BaseButton>View Details</BaseButton>
        </div>
    </div>
</template>

<style scoped>
.properties-card {
    box-shadow: var(--box-shadow);
    overflow: hidden;
    transition: all .5s ease-in-out;
    border-radius: 2.5rem 0;
    background-color: var(--white-color);
}
.card-body {
    padding: 1rem;
}
.card-body i {
    color: var(--primary-color);
}
.card-body p {
    margin: .5rem 0;
}
.properties-card .title-image {
    height: 220px;
    width: 100%;
    overflow: hidden;
}
.properties-card img {
    height: 100%;
    width: 100%;
    object-fit: cover;
    transition: all .5s ease-in-out;
}
.properties-card:hover img {
    transform: scale(1.1);
}
.properties-card ul {
    margin: .5rem 0;
    display: flex;
    gap: 1rem;
}
.properties-card .btn {
    background-color: var(--primary-color);
    color: var(--white-color);
    border-radius: 1rem 0;
    width: 100%;
}
.properties-card .btn:hover {
    background-color: var(--secondary-color);
    color: var(--primary-color);
}
</style>