<script setup>
import { useToggle } from '@vueuse/core'

const [value, toggle] = useToggle()
</script>

<template>
  <el-header
    class="relative border-b border-solid border-b-gray-200 p-0 w-full h-full bg-white dark:bg-[#242424] dark:border-b-gray-900"
  >
    <div class="flex justify-between items-center p-3">
      <a href="https://element-plus.org/en-US/">
        <span class="sr-only">Element Plus</span>
        <img
          src="../assets/logo-light.svg"
          alt="UniExplorers"
          class="block max-w-none w-[120px] h-[65px]"
        />
      </a>

      <nav>
        <ul class="hidden items-center space-x-6 lg:flex">
          <li>
            <el-link
              href="https://element-plus.org/en-US/guide/design.html"
              target="_blank"
            >
              Guide
            </el-link>
          </li>
          <li>
            <el-link
              href="https://element-plus.org/en-US/component/button.html"
              target="_blank"
            >
              Component
            </el-link>
          </li>
          <li>
            <el-link
              href="https://element-plus.org/en-US/resource/index.html"
              target="_blank"
            >
              Resource
            </el-link>
          </li>
        </ul>
      </nav>

      <div class="hidden lg:block">
        <el-button>Log in</el-button>
      </div>

      <span
        class="lg:hidden w-5 h-5 bg-white cursor-pointer dark:bg-[#242424]"
        @click="toggle()"
      >
        <a v-if="value">
          <el-icon size="20">
            <Close />
          </el-icon>
        </a>
        <a class="block relative h-full" v-else>
          <el-icon
            class="absolute -top-[6px] left-1/2 transform -translate-x-1/2"
            size="20"
            style="position: absolute"
          >
            <Minus />
          </el-icon>
          <el-icon
            class="absolute -top-[0] left-1/2 transform -translate-x-1/2"
            size="20"
            style="position: absolute"
          >
            <Minus />
          </el-icon>
          <el-icon
            class="absolute top-[6px] left-1/2 transform -translate-x-1/2"
            size="20"
            style="position: absolute"
          >
            <Minus />
          </el-icon>
        </a>
      </span>
    </div>

    <nav
      class="absolute py-4 w-full bg-white divide-y text-center lg:hidden dark:bg-[#242424] dark:divide-gray-500"
      v-if="value"
    >
      <div>
        <ul class="flex flex-col space-y-5 mb-5">
          <li>
            <el-link
              href="https://element-plus.org/en-US/guide/design.html"
              target="_blank"
            >
              Guide
            </el-link>
          </li>
          <li>
            <el-link
              href="https://element-plus.org/en-US/component/button.html"
              target="_blank"
            >
              Component
            </el-link>
          </li>
          <li>
            <el-link
              href="https://element-plus.org/en-US/resource/index.html"
              target="_blank"
            >
              Resource
            </el-link>
          </li>
        </ul>
      </div>
      <div class="pt-5">
        <el-button>Log in</el-button>
      </div>
    </nav>
  </el-header>
</template>

<style>
.el-header {
  height: 5.5em;
}
</style>