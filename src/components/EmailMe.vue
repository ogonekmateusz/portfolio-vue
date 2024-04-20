<template>

<button class="button">Email me</button>

</template>

<style scoped>
.button {
    display: inline-block;
    padding: 18px 28px;
    color: #fff;
    font-size: 18px;
    transition: all 0.3s;
    position: relative;
    z-index: 1;
    cursor: pointer;
    font-weight: bold;
    border: none;
    border: 1px solid var(--primary);
}

.button:after {
    content: "";
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: var(--primary);
    z-index: -2;
}

.button:before {
    content: "";
    position: absolute;
    bottom: 0;
    left: 0;
    width: 0%;
    height: 100%;
    background-color: var(--dark);
    transition: all 0.3s;
    z-index: -1;
}

.button:hover {
    color: var(--white);
}

.button:hover:before {
    width: 100%;
}
</style>