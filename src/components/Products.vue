<script setup>
</script>
<script>
import store from '../store';

export default {
    data() {
        return {
            panels: store.state.panels,
            check: false,
            filter: false,
            filter2: false,
        }
    },
    methods: {
        checkFunc() {
            this.check = !this.check
        },
        filterFunc(){
            this.filter = !this.filter
        },
        filterFunc2(){
            this.filter2 = !this.filter2
        }
    },
}
</script>

<template>
    <div class="productBlock min-h-[600px] w-[100%] bg-[#012465]">
        <div class="h-[100%] w-[100%] flex">

            <div class="filterProduct w-[385px] h-[max-content] sticky top-[130px] pt-[51px] pl-[80px]">
                <ul class="">
                    <li class="text-[#fff] mb-[20px]">Product type</li>

                    <button @click="checkFunc" class="mb-[12px] flex items-center ">

                        <div :class="{ checkActive: this.check == true }"
                            class="h-[16px] w-[16px] border-[1px] border-solid border-[#4269E2] rounded-[2px]"></div>
                        <p class="text-[#fff] ml-[12px]">Монокристаллические</p>
                    </button>

                    <button @click="checkFunc" class="mb-[12px] flex items-center ">

                        <div :class="{ checkActive: this.check == true }"
                            class="h-[16px] w-[16px] border-[1px] border-solid border-[#4269E2] rounded-[2px]"></div>
                        <p class="text-[#fff] ml-[12px]">Высокая эффективность</p>
                    </button>

                    <button @click="checkFunc" class="mb-[12px] flex items-center ">

                        <div :class="{ checkActive: this.check == true }"
                            class="h-[16px] w-[16px] border-[1px] border-solid border-[#4269E2] rounded-[2px]"></div>
                        <p class="text-[#fff] ml-[12px]">Эстетичный внешний вид</p>
                    </button>

                    <button @click="checkFunc" class="mb-[12px] flex items-center ">

                        <div :class="{ checkActive: this.check == true }"
                            class="h-[16px] w-[16px] border-[1px] border-solid border-[#4269E2] rounded-[2px]"></div>
                        <p class="text-[#fff] ml-[12px]">Поликристаллические</p>
                    </button>

                    <button @click="checkFunc" class="mb-[12px] flex items-center ">

                        <div :class="{ checkActive: this.check == true }"
                            class="h-[16px] w-[16px] border-[1px] border-solid border-[#4269E2] rounded-[2px]"></div>
                        <p class="text-[#fff] ml-[12px]">Тонкопленочные</p>
                    </button>

                    <button @click="checkFunc" class="mb-[12px] flex items-center ">

                        <div :class="{ checkActive: this.check == true }"
                            class="h-[16px] w-[16px] border-[1px] border-solid border-[#4269E2] rounded-[2px]"></div>
                        <p class="text-[#fff] ml-[12px]">Малый вес</p>
                    </button>


                </ul>
                <ul class="mt-[48px]">
                    <li class="text-[#fff] mb-[20px]">Price</li>
                    <button @click="checkFunc" class="mb-[12px] flex items-center ">

                        <div :class="{ checkActive: this.check == true }"
                            class="h-[16px] w-[16px] border-[1px] border-solid border-[#4269E2] rounded-[2px]"></div>
                        <p class="text-[#fff] ml-[12px]">0 - 100</p>
                    </button>

                    <button @click="checkFunc" class="mb-[12px] flex items-center ">

                        <div :class="{ checkActive: this.check == true }"
                            class="h-[16px] w-[16px] border-[1px] border-solid border-[#4269E2] rounded-[2px]"></div>
                        <p class="text-[#fff] ml-[12px]">100 - 250</p>
                    </button>

                    <button @click="checkFunc" class="mb-[12px] flex items-center ">

                        <div :class="{ checkActive: this.check == true }"
                            class="h-[16px] w-[16px] border-[1px] border-solid border-[#4269E2] rounded-[2px]"></div>
                        <p class="text-[#fff] ml-[12px]">250+</p>
                    </button>

                </ul>
            </div>
<!-- при адаптиве -->

<div  class="filter_block flex absolute mt-[20px] left-[50%] translate-x-[-50%]">
                <div @click="filterFunc" class="filter__menu h-[56px] mr-[20px] w-[250px] relative bg-[#f9f9f9] flex items-center justify-center">
                    Filters <img class="ml-[12px]" src="../assets/icons/Caret--down.png" alt="">
                </div>
                <div @click="filterFunc2" class="filter__menu  h-[56px] mr-[20px] w-[250px] relative bg-[#f9f9f9] flex items-center justify-center">
                    Sorting <img class="ml-[12px]" src="../assets/icons/Caret--down.png" alt="">
                </div>
            </div>
<!--  -->
            <div :class="{filterActive: this.filter == true}" class="filter_m h-[100px] w-[250px] bg-[#f9f9f9] z-[99] absolute mt-[76px] ml-[114px]">
                <ul class="filter-m__ul">
                    <button @click="checkFunc" class="mb-[12px] flex items-center ">

                        <div :class="{ checkActive: this.check == true }"
                            class="h-[16px] w-[16px] border-[1px] border-solid border-[#4269E2] rounded-[2px]"></div>
                        <p class="tex text-[#000] ml-[12px]">Монокри</p>
                    </button>
                    <button @click="checkFunc" class="mb-[12px] flex items-center ">

                        <div :class="{ checkActive: this.check == true }"
                            class="h-[16px] w-[16px] border-[1px] border-solid border-[#4269E2] rounded-[2px]"></div>
                        <p class="tex text-[#000] ml-[12px]">Моно</p>
                    </button>
                </ul>
            </div>

            <div :class="{filterActive: this.filter2 == true}" class="filter_m filter2 h-[100px] w-[250px] bg-[#f9f9f9] z-[99] absolute mt-[76px] ml-[374px]">
                <ul class="filter-m__ul">
                    <button @click="checkFunc" class="mb-[12px] flex items-center ">

                        <div :class="{ checkActive: this.check == true }"
                            class="h-[16px] w-[16px] border-[1px] border-solid border-[#4269E2] rounded-[2px]"></div>
                        <p class="text-[#000] ml-[12px]">0-100</p>
                    </button>
                    <button @click="checkFunc" class="mb-[12px] flex items-center ">

                        <div :class="{ checkActive: this.check == true }"
                            class="h-[16px] w-[16px] border-[1px] border-solid border-[#4269E2] rounded-[2px]"></div>
                        <p class="text-[#000] ml-[12px]">100 - 250</p>
                    </button>
                </ul>
            </div>
            <!--  -->

            


        <!-- при адаптиве -->

            <div class="productItems flex-1 pb-[120px] bg-[#fff] pl-[45px] flex flex-wrap">

                <div v-for="i of this.panels" :key="i.id"
                    class="productAll h-[462px] w-[305px] text-[#2A254B] mr-[20px] mt-[37px]">
                    <img class="productImg h-[376px] w-[305px]" :src="i.img" alt="">
                    <div class="flex justify-between mt-[24px] text-center h-[30px] items-center">
                        <h2 class="text-[20px] text-[#2A254B]">{{ i.title }}</h2>
                        <span class="text-[14px]">{{ i.wat }}W</span>
                    </div>
                    <p class="mt-[8px] text-[18px]">{{ i.price }}$</p>
                </div>



            </div>

        </div>
    </div>
</template>

<style>
.checkActive {
    background: #4269E2;
    background-image: url('@/assets/icons/checkbox.png');
    background-repeat: no-repeat;
    background-size: contain;
    background-position: center center;
}
.filterActive{
    display: block;
}
</style>