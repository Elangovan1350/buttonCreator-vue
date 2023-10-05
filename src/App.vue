<script setup>
import { reactive, ref } from "vue";

const width = ref("70");
const height = ref("70");
const radius = ref("0");
const border = ref("0");
const bgcolor = ref("");
const fncolor = ref("");

const font = ref("16")

const button = reactive({
  name: "",
});
</script>

<template>
  <div class="first">
    <div class="second">
      <button
        :style="{
          width: width + 'px',
          height: height + 'px',
          borderRadius: radius + '%',
          background: bgcolor,
          borderWidth: border + 'px',
          fontSize:font+'px',
          color:fncolor,
        }"
      >
        {{ button.name }}
      </button>
    </div>
    <div class="third">
      <label for=""
        >Button Name:
        <input type="text" v-model="button.name" />
      </label>
      <label for=""
        >width :
        <input
          type="range"
          name="size"
          id="size"
          min="30"
          max="300"
          v-model="width"
        />
      </label>
      <label for=""
        >height :
        <input
          type="range"
          name="size"
          id="size"
          min="30"
          max="300"
          v-model="height"
        />
      </label>
      <label for=""
        >border radius :
        <input
          type="range"
          name="size"
          id="size"
          min="0"
          max="50"
          v-model="radius"
        />
      </label>
      <label for=""
        >border radius :
        <input
          type="range"
          name="size"
          id="size"
          min="0"
          max="20"
          v-model="border"
        />
      </label>
      <label for=""
        >font size :
        <input
          type="range"
          name="size"
          id="size"
          min="0"
          max="40"
          v-model="font"
        />
      </label>
      <label for=""
        >font color:
        <input type="color" name="" id="" v-model="fncolor" />
      </label>
      <label for=""
        >background color:
        <input type="color" name="" id="" v-model="bgcolor" />
      </label>
    </div>
  </div>
</template>

<style scoped>
.first {
  display: flex;
  flex-direction: column;
  height: 100vh;
  width: 100vw;
}

.second {
  height: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.third {
  height: 50%;
  display: flex;
  flex-direction: column;
  margin-left: 10px;
  text-transform: capitalize;
}
</style>
