<template>
    <div>
        <p>Capacity: {{ capacity }} ({{ spacesLeft }} spaces)</p>
        <button @click="increaseCapacity()">Increase Capacity</button>
        <h2>Attending</h2>
        <ul>
        <li v-for="(name, index) in attending" :key="index">
            {{ name }}
        </li>
        </ul>
  </div>
</template>
<script>
    import { ref, computed } from "vue";
    export default {
        setup() {
            return useEventSpace();
        }
    };

    function useEventSpace() {
        const capacity = ref(4);
        const attending = ref(["Tim", "Bob", "Joe"]);
        const spacesLeft = computed(() => {
            return capacity.value - attending.value.length;
        });
        function increaseCapacity() {
            capacity.value++;
        }
        return { capacity, attending, spacesLeft, increaseCapacity };
    }
</script>