<template>
    <button class="button" :class="`button-color--${colors}`">
        <a>{{label}}</a>
    </button>
</template>

<script>
export default {
    name: 'Button',
    props: {
        id:{
          type: Number,
          default: 1
        },
        colors: {
            type: String,
            default: 'normal', // 'normal' or 'primary'
        },
        label: {
            type: String,
            default: 'Default String',
        },
    },
};
</script>

<style scoped>
.button {
    appearance: none;
    border: none;
    font-family: sans-serif;
    padding: 8px 16px;
    margin: 12px;
    border-radius: 2px;
}

.button-color--normal {
    background-color: #eee;
    color: #222;
}

.button-color--normal:hover,
.button-color--normal:focus {
    background-color: #e0e0e0;
}

.button-color--normal:active {
    background-color: #bdbdbd;
}

.button-color--primary {
    background-color: #2196f3;
    color: #fff;
}

.button-color--primary:hover,
.button-color--primary:focus {
    background-color: #1e88e5;
}

.button-color--primary:active {
    background-color: #1976D2;
}
</style>