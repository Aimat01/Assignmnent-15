<template>
    <div class="container">
        <div class="dropdown">
            <button @click="toggleDropdown" class="dropbtn">Dropdown</button>
            <div :class="{ 'dropdown-content': true, 'show': showDropdown }">
                <select v-model="selectedOption">
                    <option disabled value="">Select an option</option>
                    <option v-for="option in options" :key="option">{{ option }}</option>
                </select>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            showDropdown: false,
            selectedOption: '',
            options: ['Option1', 'Option2', 'Option3', 'Option4']
        };
    },
    methods: {
        toggleDropdown() {
            this.showDropdown = !this.showDropdown;
        }
    }
}
</script>

<style>
.container {
    display: flex;
    justify-content: center;
    padding-top: 40px;
}

.dropdown {
    position: relative;
    display: inline-block;
}

.dropbtn {
    font-size: 16px;
    border: none;
    cursor: pointer;
}

.dropdown-content {
    display: none;
    position: absolute;
    min-width: 160px;
    z-index: 1;
}

.dropdown-content.select {
    width: 100%;
    padding: 5px;
    border: none;
    outline: none;
}

.dropdown-content.select:focus {
    background-color: #ddd;
}

.show {
    display: block;
}
</style>
