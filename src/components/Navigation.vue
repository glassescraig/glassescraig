<template>
  <div class="relative bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 mt-0">
      <div
        class="
          flex
          justify-between
          items-center
          border-b-2 border-gray-100
          py-6
          md:justify-start
          md:space-x-10
        "
      >
        <div class="flex justify-start lg:w-0 lg:flex-1">
          <a href="#">
            <span class="sr-only">Workflow</span>
            <img
              class="h-8 w-auto sm:h-10"
              src="https://tailwindui.com/img/logos/workflow-mark-indigo-600.svg"
              alt=""
            />
          </a>
        </div>
        <div class="-mr-2 -my-2 md:hidden">
          <button
            type="button"
            class="
              bg-white
              rounded-md
              p-2
              inline-flex
              items-center
              justify-center
              text-gray-400
              hover:text-gray-500
              hover:bg-gray-100
              focus:outline-none
              focus:ring-2 focus:ring-inset focus:ring-indigo-500
            "
            @click="isOpen = !isOpen"
          >
            <span class="sr-only">Open menu</span>
            <!-- Heroicon name: outline/menu -->
            <svg
              class="h-6 w-6"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
              aria-hidden="true"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M4 6h16M4 12h16M4 18h16"
              />
            </svg>
          </button>
        </div>
        <nav class="hidden md:flex space-x-10">
          <div class="relative">
            <!-- Item active: "text-gray-900", Item inactive: "text-gray-500" -->
            <button
              type="button"
              class="
                text-gray-500
                group
                bg-white
                rounded-md
                inline-flex
                items-center
                text-base
                font-medium
                hover:text-gray-900
                focus:outline-none
                focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500
              "
            >
            <!-- https://reactgo.com/scroll-to-anchor-tags-vue-router/ -->
              <span>About</span>
            </button>

            <div
              class="
                absolute
                z-10
                -ml-4
                mt-3
                transform
                px-2
                w-screen
                max-w-md
                sm:px-0
                lg:ml-0
                lg:left-1/2
                lg:-translate-x-1/2
              "
            >
              <div
                class="
                  rounded-lg
                  shadow-lg
                  ring-1 ring-black ring-opacity-5
                  overflow-hidden
                "
              >
              </div>
            </div>
          </div>

          <a
            href="#"
            class="text-base font-medium text-gray-500 hover:text-gray-900"
          >
            Example
          </a>
          <a
            href="#"
            class="text-base font-medium text-gray-500 hover:text-gray-900"
          >
            Docs
          </a>

        </nav>
        <div class="hidden md:flex items-center justify-end md:flex-1 lg:w-0">
          <a
            href="#"
            class="
              whitespace-nowrap
              text-base
              font-medium
              text-gray-500
              hover:text-gray-900
            "
          >
            Sign in
          </a>
          <a
            href="#"
            class="
              ml-8
              whitespace-nowrap
              inline-flex
              items-center
              justify-center
              px-4
              py-2
              border border-transparent
              rounded-md
              shadow-sm
              text-base
              font-medium
              text-white
              bg-indigo-600
              hover:bg-indigo-700
            "
          >
            Sign up
          </a>
        </div>
      </div>
    </div>

    <!--Mobile menu, show/hide based on mobile menu state.-->
  <div class="sm:hidden" :class="isOpen ? 'block' : 'hidden'" id="mobile-menu">
    <div class="px-2 pt-2 pb-3 space-y-1">
      <!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->
      <a href="#" class="bg-gray-900 text-white block px-3 py-2 rounded-md text-base font-medium" aria-current="page">Dashboard</a>

      <a href="#" class="text-gray-300 hover:bg-gray-700 hover:text-white block px-3 py-2 rounded-md text-base font-medium">Team</a>

      <a href="#" class="text-gray-300 hover:bg-gray-700 hover:text-white block px-3 py-2 rounded-md text-base font-medium">Projects</a>

      <a href="#" class="text-gray-300 hover:bg-gray-700 hover:text-white block px-3 py-2 rounded-md text-base font-medium">Calendar</a>
    </div>
  </div>
  </div>
</template>

<script>
export default {
  name: "Navigation",
  data() {
    return {
      isOpen: false,
    }
  },
};
</script>