<template>
    <!-- first menu -->
    <v-app-bar height="80">
        <v-container align="center">
            <v-row dense justify="center">
                <v-col cols="4">
                    <a href="#">
                        <v-img
                            class="mt-3"
                            width="100"
                            src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/69/Airbnb_Logo_B%C3%A9lo.svg/1200px-Airbnb_Logo_B%C3%A9lo.svg.png"
                        ></v-img>
                    </a>
                </v-col>

                <v-col cols="4">
                    <v-btn
                        rounded
                        elevation="2"
                        value="expand-dialog"
                        height="50"
                    >
                        <a href="#" class="ml-n2" style="text-decoration: none">
                            <v-icon
                                class="bg-error"
                                icon="mdi-magnify"
                                style="
                                    border-radius: 50%;
                                    width: 35px;
                                    height: 35px;
                                    font-size: 20px;
                                "
                            ></v-icon>
                        </a>
                        <div
                            class="btn-area"
                            v-for="(name, index) in threechoice"
                            :key="index"
                        >
                            <p>{{ name }}</p>
                        </div>
                    </v-btn>
                </v-col>

                <v-col cols="4">
                    <v-btn
                        rounded
                        height="40px"
                        style="text-transform: capitalize"
                    >
                        Airbnb Your home</v-btn
                    >
                    <v-btn style="border-radius: 50%" height="50" rounded>
                        <v-icon icon="mdi-web" style="font-size: 30px"></v-icon>
                    </v-btn>

                    <v-menu open-on-hover transition="slide-y-transition">
                        <template v-slot:activator="{ props }">
                            <v-btn
                                v-bind="props"
                                class="ml-3"
                                elevation="2"
                                rounded
                            >
                                <div
                                    style="
                                        display: flex;
                                        gap: 5px;
                                        font-size: 20px;
                                    "
                                >
                                    <v-icon icon="mdi-menu"></v-icon>
                                    <v-icon
                                        style="color: grey"
                                        icon="mdi-account-circle"
                                    ></v-icon>
                                </div>
                            </v-btn>
                        </template>
                        <v-list width="200" class="ml-n16 mt-4">
                            <v-list-item v-for="(item, i) in items1" :key="i">
                                <v-list-item-title
                                    ><a
                                        href="#"
                                        style="
                                            text-decoration: none;
                                            color: black;
                                        "
                                        >{{ item.title }}</a
                                    ></v-list-item-title
                                >
                            </v-list-item>
                            <hr />
                            <v-list-item v-for="(item, i) in items2" :key="i">
                                <v-list-item-title
                                    ><a
                                        href="#"
                                        style="
                                            text-decoration: none;
                                            color: black;
                                        "
                                        >{{ item.title }}</a
                                    >
                                </v-list-item-title>
                            </v-list-item>
                        </v-list>
                    </v-menu>
                </v-col>
            </v-row>
        </v-container>
    </v-app-bar>

    <!-- menu categories -->
    <v-app-bar height="90">
        <v-container>
            <v-row>
                <v-col cols="11">
                    <v-sheet cycle class="mx-auto">
                        <v-slide-group show-arrows>
                            <v-slide-group-item>
                                <v-tabs v-model="tab">
                                    <v-tab value="one">
                                        <div class="tabstyle">
                                            <v-img
                                                width="20"
                                                src="https://a0.muscache.com/pictures/6ad4bd95-f086-437d-97e3-14d12155ddfe.jpg"
                                            ></v-img>
                                            <p>countryside</p>
                                        </div>
                                    </v-tab>

                                    <v-tab value="two">
                                        <div class="tabstyle">
                                            <v-img
                                                width="20"
                                                src="https://a0.muscache.com/pictures/3fb523a0-b622-4368-8142-b5e03df7549b.jpg"
                                            ></v-img>
                                            <p>amazing pools</p>
                                        </div>
                                    </v-tab>

                                    <v-tab value="three">
                                        <div class="tabstyle">
                                            <v-img
                                                width="20"
                                                src="https://a0.muscache.com/pictures/aaa02c2d-9f0d-4c41-878a-68c12ec6c6bd.jpg"
                                            ></v-img>
                                            <p>farms</p>
                                        </div>
                                    </v-tab>

                                    <v-tab value="four">
                                        <div class="tabstyle">
                                            <v-img
                                                width="20"
                                                src="https://a0.muscache.com/pictures/4221e293-4770-4ea8-a4fa-9972158d4004.jpg"
                                            ></v-img>
                                            <p>caves</p>
                                        </div>
                                    </v-tab>

                                    <v-tab value="five">
                                        <div class="tabstyle">
                                            <v-img
                                                width="20"
                                                src="https://a0.muscache.com/pictures/ee9e2a40-ffac-4db9-9080-b351efc3cfc4.jpg"
                                            ></v-img>
                                            <p>tropical</p>
                                        </div>
                                    </v-tab>

                                    <v-tab value="six">
                                        <div class="tabstyle">
                                            <v-img
                                                width="20"
                                                src="https://a0.muscache.com/pictures/0ff9740e-52a2-4cd5-ae5a-94e1bfb560d6.jpg"
                                            ></v-img>
                                            <p>containers</p>
                                        </div>
                                    </v-tab>

                                    <v-tab value="seven">
                                        <div class="tabstyle">
                                            <v-img
                                                width="20"
                                                src="https://a0.muscache.com/pictures/eb7ba4c0-ea38-4cbb-9db6-bdcc8baad585.jpg"
                                            ></v-img>
                                            <p>private rooms</p>
                                        </div>
                                    </v-tab>

                                    <v-tab value="eight">
                                        <div class="tabstyle">
                                            <v-img
                                                width="20"
                                                src="https://a0.muscache.com/pictures/50861fca-582c-4bcc-89d3-857fb7ca6528.jpg"
                                            ></v-img>
                                            <p>design</p>
                                        </div>
                                    </v-tab>

                                    <v-tab value="nine">
                                        <div class="tabstyle">
                                            <v-img
                                                width="20"
                                                src="https://a0.muscache.com/pictures/1b6a8b70-a3b6-48b5-88e1-2243d9172c06.jpg"
                                            ></v-img>
                                            <p>castle</p>
                                        </div>
                                    </v-tab>

                                    <v-tab value="ten">
                                        <div class="tabstyle">
                                            <v-img
                                                width="20"
                                                src="https://a0.muscache.com/pictures/687a8682-68b3-4f21-8d71-3c3aef6c1110.jpg"
                                            ></v-img>
                                            <p>boats</p>
                                        </div>
                                    </v-tab>

                                    <v-tab value="eleven">
                                        <div class="tabstyle">
                                            <v-img
                                                width="20"
                                                src="https://a0.muscache.com/pictures/10ce1091-c854-40f3-a2fb-defc2995bcaf.jpg"
                                            ></v-img>
                                            <p>beach</p>
                                        </div>
                                    </v-tab>

                                    <v-tab value="twelve">
                                        <div class="tabstyle">
                                            <v-img
                                                width="20"
                                                src="https://a0.muscache.com/pictures/8b44f770-7156-4c7b-b4d3-d92549c8652f.jpg"
                                            ></v-img>
                                            <p>arctic</p>
                                        </div>
                                    </v-tab>

                                    <v-tab value="thirteen">
                                        <div class="tabstyle">
                                            <v-img
                                                width="20"
                                                src="https://a0.muscache.com/pictures/8e507f16-4943-4be9-b707-59bd38d56309.jpg"
                                            ></v-img>
                                            <p>islands</p>
                                        </div>
                                    </v-tab>

                                    <v-tab value="fourteen">
                                        <div class="tabstyle">
                                            <v-img
                                                width="20"
                                                src="https://a0.muscache.com/pictures/732edad8-3ae0-49a8-a451-29a8010dcc0c.jpg"
                                            ></v-img>
                                            <p>cabins</p>
                                        </div>
                                    </v-tab>

                                    <v-tab value="fifteen">
                                        <div class="tabstyle">
                                            <v-img
                                                width="20"
                                                src="https://a0.muscache.com/pictures/957f8022-dfd7-426c-99fd-77ed792f6d7a.jpg"
                                            ></v-img>
                                            <p>surfing</p>
                                        </div>
                                    </v-tab>

                                    <v-tab value="sixteen">
                                        <div class="tabstyle">
                                            <v-img
                                                width="20"
                                                src="https://a0.muscache.com/pictures/248f85bf-e35e-4dc3-a9a1-e1dbff9a3db4.jpg"
                                            ></v-img>
                                            <p>top of the world</p>
                                        </div>
                                    </v-tab>

                                    <v-tab value="seventeen">
                                        <div class="tabstyle">
                                            <v-img
                                                width="20"
                                                src="https://a0.muscache.com/pictures/4d4a4eba-c7e4-43eb-9ce2-95e1d200d10e.jpg"
                                            ></v-img>
                                            <p>tree house</p>
                                        </div>
                                    </v-tab>
                                </v-tabs>
                            </v-slide-group-item>
                        </v-slide-group>
                    </v-sheet>
                </v-col>

                <v-col cols="1">
                    <v-window v-model="tab">
                        <v-window-item value="one">
                            <v-dialog
                                transition="dialog-bottom-transition"
                                v-model="dialog"
                                scrollable
                                width="auto"
                            >
                                <template v-slot:activator="{ props }">
                                    <v-btn
                                        v-bind="props"
                                        variant="outlined"
                                        width="120px"
                                        height="50px"
                                        class="mt-5"
                                        style="
                                            text-transform: capitalize;
                                            border-radius: 10px;
                                        "
                                    >
                                        <v-icon
                                            icon="mdi-swap-horizontal"
                                            style="font-size: 30px"
                                        ></v-icon>
                                        &nbsp;&nbsp; filters
                                    </v-btn>
                                </template>
                                <template v-slot:default="{ isActive }">
                                    <v-card width="900px">
                                        <v-card-title
                                            class="d-flex pa-3 text-center justify-space-around"
                                            style="font-size: 30px"
                                        >
                                            <v-btn
                                                style="
                                                    font-size: 30px;
                                                    color: red;
                                                "
                                                variant="text"
                                                @click="isActive.value = false"
                                            >
                                                <v-icon
                                                    icon="mdi-close-thick"
                                                ></v-icon>
                                            </v-btn>
                                            <h4>Filter</h4>
                                        </v-card-title>
                                        <v-divider></v-divider>

                                        <v-card-text>
                                            <!-- Section 1 -->
                                            <div
                                                style="
                                                    font-size: 25px;
                                                    padding-top: 20px;
                                                    font-weight: bold;
                                                "
                                            >
                                                Price Range
                                            </div>
                                            <div style="color: grey">
                                                The average total price for 5
                                                nights is ‎$1,229
                                            </div>

                                            <v-row
                                                dense
                                                justify="space-around"
                                                class="pt-6"
                                            >
                                                <v-col cols="5">
                                                    <small style="color: grey">
                                                        min price</small
                                                    >
                                                    <v-text-field
                                                        variant="outlined"
                                                        type="text"
                                                    >
                                                        $&nbsp;&nbsp;50
                                                    </v-text-field>
                                                </v-col>
                                                <v-col cols="2">
                                                    <h1
                                                        align="center"
                                                        class="pt-6"
                                                    >
                                                        -
                                                    </h1></v-col
                                                >
                                                <v-col cols="5">
                                                    <small style="color: grey">
                                                        max price</small
                                                    >
                                                    <v-text-field
                                                        variant="outlined"
                                                        type="text"
                                                    >
                                                        $&nbsp;&nbsp;3800+
                                                    </v-text-field>
                                                </v-col>
                                            </v-row>
                                            <v-divider></v-divider>

                                            <!-- Section 2 -->
                                            <div
                                                style="
                                                    font-size: 25px;
                                                    padding-top: 30px;
                                                    font-weight: bold;
                                                "
                                            >
                                                Type of place
                                            </div>
                                            <v-row dense justify="space-around">
                                                <v-col cols="6">
                                                    <v-list-item
                                                        title="Entire Place"
                                                        subtitle="A place all to yourself"
                                                    >
                                                        <template
                                                            v-slot:prepend
                                                        >
                                                            <v-checkbox
                                                                style="
                                                                    font-size: 20px;
                                                                    padding-right: 10px;
                                                                "
                                                                class="ml-n5"
                                                            ></v-checkbox>
                                                        </template>
                                                    </v-list-item>
                                                </v-col>

                                                <v-col cols="6">
                                                    <v-list-item
                                                        title="Private Room"
                                                        subtitle="Your own room in a home or a hotel, plus some shared common spaces"
                                                    >
                                                        <template
                                                            v-slot:prepend
                                                        >
                                                            <v-checkbox
                                                                style="
                                                                    font-size: 20px;
                                                                    padding-right: 10px;
                                                                "
                                                            ></v-checkbox>
                                                        </template>
                                                    </v-list-item>
                                                </v-col>

                                                <v-col cols="12" class="mt-n2">
                                                    <v-list-item
                                                        title="Shared Room"
                                                        subtitle="A sleeping space and common areas that may be shared with others"
                                                    >
                                                        <template
                                                            v-slot:prepend
                                                        >
                                                            <v-checkbox
                                                                style="
                                                                    font-size: 20px;
                                                                    padding-right: 10px;
                                                                "
                                                                class="ml-n5"
                                                            ></v-checkbox>
                                                        </template>
                                                    </v-list-item>
                                                </v-col>
                                            </v-row>
                                            <v-divider></v-divider>

                                            <!-- Section 3 -->
                                            <div
                                                style="
                                                    font-size: 25px;
                                                    padding-top: 30px;
                                                    font-weight: bold;
                                                "
                                            >
                                                Rooms and Beds
                                            </div>
                                            <div style="margin-top: 30px">
                                                Bedrooms
                                            </div>
                                            <v-row dense justify="space-around">
                                                <v-col cols="12" class="pt-5">
                                                    <v-btn-toggle
                                                        v-model="bedroom"
                                                        color="black"
                                                        style="gap: 10px"
                                                    >
                                                        <v-btn
                                                            value="bedroom1"
                                                            style="
                                                                border-radius: 23px;
                                                                text-transform: capitalize;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                            >Any
                                                        </v-btn>
                                                        <v-btn
                                                            value="bedroom2"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            1
                                                        </v-btn>
                                                        <v-btn
                                                            value="bedroom3"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            2
                                                        </v-btn>
                                                        <v-btn
                                                            value="bedroom4"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            3
                                                        </v-btn>
                                                        <v-btn
                                                            value="bedroom5"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            4
                                                        </v-btn>
                                                        <v-btn
                                                            value="bedroom6"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            5
                                                        </v-btn>
                                                        <v-btn
                                                            value="bedroom7"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            6
                                                        </v-btn>
                                                        <v-btn
                                                            value="bedroom8"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            7
                                                        </v-btn>
                                                        <v-btn
                                                            value="bedroom9"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            8+
                                                        </v-btn>
                                                    </v-btn-toggle>
                                                </v-col>
                                            </v-row>

                                            <div style="margin-top: 30px">
                                                Bed
                                            </div>
                                            <v-row dense justify="space-around">
                                                <v-col cols="12" class="pt-5">
                                                    <v-btn-toggle
                                                        v-model="bed"
                                                        color="black"
                                                        style="gap: 10px"
                                                    >
                                                        <v-btn
                                                            value="bed1"
                                                            style="
                                                                border-radius: 23px;
                                                                text-transform: capitalize;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                            >Any
                                                        </v-btn>
                                                        <v-btn
                                                            value="bed2"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            1
                                                        </v-btn>
                                                        <v-btn
                                                            value="bed3"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            2
                                                        </v-btn>
                                                        <v-btn
                                                            value="bed4"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            3
                                                        </v-btn>
                                                        <v-btn
                                                            value="bed5"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            4
                                                        </v-btn>
                                                        <v-btn
                                                            value="bed6"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            5
                                                        </v-btn>
                                                        <v-btn
                                                            value="bed7"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            6
                                                        </v-btn>
                                                        <v-btn
                                                            value="bed8"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            7
                                                        </v-btn>
                                                        <v-btn
                                                            value="bed9"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            8+
                                                        </v-btn>
                                                    </v-btn-toggle>
                                                </v-col>
                                            </v-row>

                                            <div style="margin-top: 30px">
                                                Bathrooms
                                            </div>
                                            <v-row dense justify="space-around">
                                                <v-col cols="12" class="pt-5">
                                                    <v-btn-toggle
                                                        v-model="bath"
                                                        color="black"
                                                        style="gap: 10px"
                                                    >
                                                        <v-btn
                                                            value="bath1"
                                                            style="
                                                                border-radius: 23px;
                                                                text-transform: capitalize;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                            >Any
                                                        </v-btn>
                                                        <v-btn
                                                            value="bath2"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            1
                                                        </v-btn>
                                                        <v-btn
                                                            value="bath3"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            2
                                                        </v-btn>
                                                        <v-btn
                                                            value="bath4"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            3
                                                        </v-btn>
                                                        <v-btn
                                                            value="bath5"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            4
                                                        </v-btn>
                                                        <v-btn
                                                            value="bath6"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            5
                                                        </v-btn>
                                                        <v-btn
                                                            value="bath7"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            6
                                                        </v-btn>
                                                        <v-btn
                                                            value="bath8"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            7
                                                        </v-btn>
                                                        <v-btn
                                                            value="bath9"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            8+
                                                        </v-btn>
                                                    </v-btn-toggle>
                                                </v-col>
                                            </v-row>
                                            <v-divider
                                                class="mt-14"
                                            ></v-divider>

                                            <!-- Section 4 -->
                                            <div
                                                style="
                                                    font-size: 25px;
                                                    padding-top: 30px;
                                                    font-weight: bold;
                                                "
                                            >
                                                Property Type
                                            </div>
                                            <v-row
                                                dense
                                                justify="center"
                                                class="mt-5"
                                            >
                                                <v-col cols="3">
                                                    <v-btn
                                                        class="hoverbtn"
                                                        height="130"
                                                        width="170"
                                                        style="
                                                            border-radius: 15px;
                                                        "
                                                    >
                                                        <div
                                                            style="
                                                                display: flex;
                                                                flex-direction: column;
                                                                gap: 20px;
                                                                transition: 0.3s;
                                                            "
                                                        >
                                                            <v-img
                                                                width="50px"
                                                                src="https://a0.muscache.com/pictures/4d7580e1-4ab2-4d26-a3d6-97f9555ba8f9.jpg"
                                                            ></v-img>
                                                            <p>House</p>
                                                        </div>
                                                    </v-btn>
                                                </v-col>

                                                <v-col cols="3">
                                                    <v-btn
                                                        class="hoverbtn"
                                                        height="130"
                                                        width="170"
                                                        style="
                                                            border-radius: 15px;
                                                        "
                                                    >
                                                        <div
                                                            style="
                                                                display: flex;
                                                                flex-direction: column;
                                                                gap: 20px;
                                                                transition: 0.3s;
                                                            "
                                                        >
                                                            <v-img
                                                                width="50px"
                                                                src="https://a0.muscache.com/pictures/21cfc7c9-5457-494d-9779-7b0c21d81a25.jpg"
                                                            ></v-img>
                                                            <p>Apartment</p>
                                                        </div>
                                                    </v-btn>
                                                </v-col>

                                                <v-col cols="3">
                                                    <v-btn
                                                        class="hoverbtn"
                                                        height="130"
                                                        width="170"
                                                        style="
                                                            border-radius: 15px;
                                                        "
                                                    >
                                                        <div
                                                            style="
                                                                display: flex;
                                                                flex-direction: column;
                                                                gap: 20px;
                                                                transition: 0.3s;
                                                            "
                                                        >
                                                            <v-img
                                                                width="50px"
                                                                src="https://a0.muscache.com/pictures/6f261426-2e47-4c91-8b1a-7a847da2b21b.jpg"
                                                            ></v-img>
                                                            <p>Guesthouse</p>
                                                        </div>
                                                    </v-btn>
                                                </v-col>

                                                <v-col cols="3">
                                                    <v-btn
                                                        class="hoverbtn"
                                                        height="130"
                                                        width="170"
                                                        style="
                                                            border-radius: 15px;
                                                        "
                                                    >
                                                        <div
                                                            style="
                                                                display: flex;
                                                                flex-direction: column;
                                                                gap: 20px;
                                                                transition: 0.3s;
                                                            "
                                                        >
                                                            <v-img
                                                                width="50px"
                                                                src="https://a0.muscache.com/pictures/64b27fed-56a1-4f03-950a-d8da08efb428.jpg"
                                                            ></v-img>
                                                            <p>Hotel</p>
                                                        </div>
                                                    </v-btn>
                                                </v-col>
                                            </v-row>
                                            <v-divider
                                                class="mt-14"
                                            ></v-divider>

                                            <!-- Section 5 -->
                                            <div
                                                style="
                                                    font-size: 25px;
                                                    padding-top: 30px;
                                                    font-weight: bold;
                                                "
                                            >
                                                Amenities
                                            </div>
                                            <h4 class="mt-10">Essentials</h4>
                                            <v-row
                                                dense
                                                justify="space-between"
                                                class="mt-5 ml-n3"
                                            >
                                                <v-col cols="6">
                                                    <v-checkbox
                                                        style="
                                                            font-size: 20px;
                                                            padding-right: 10px;
                                                        "
                                                        label="Wifi"
                                                    ></v-checkbox>
                                                </v-col>

                                                <v-col cols="6">
                                                    <v-checkbox
                                                        style="
                                                            font-size: 20px;
                                                            padding-right: 10px;
                                                        "
                                                        label="Kitchen"
                                                    ></v-checkbox>
                                                </v-col>
                                            </v-row>

                                            <v-row
                                                dense
                                                justify="space-between"
                                                class="mt-n6 ml-n3"
                                            >
                                                <v-col cols="6">
                                                    <v-checkbox
                                                        style="
                                                            font-size: 20px;
                                                            padding-right: 10px;
                                                        "
                                                        label="Washer"
                                                    ></v-checkbox>
                                                </v-col>

                                                <v-col cols="6">
                                                    <v-checkbox
                                                        style="
                                                            font-size: 20px;
                                                            padding-right: 10px;
                                                        "
                                                        label="Dryer"
                                                    ></v-checkbox>
                                                </v-col>
                                            </v-row>

                                            <v-row
                                                dense
                                                justify="space-between"
                                                class="mt-n6 ml-n3"
                                            >
                                                <v-col cols="6">
                                                    <v-checkbox
                                                        style="
                                                            font-size: 20px;
                                                            padding-right: 10px;
                                                        "
                                                        label="Aire Conditioning"
                                                    ></v-checkbox>
                                                </v-col>

                                                <v-col cols="6">
                                                    <v-checkbox
                                                        style="
                                                            font-size: 20px;
                                                            padding-right: 10px;
                                                        "
                                                        label="Jeating"
                                                    ></v-checkbox>
                                                </v-col>
                                            </v-row>
                                            <v-divider></v-divider>

                                            <!-- Section 6 -->
                                            <div
                                                style="
                                                    font-size: 25px;
                                                    padding-top: 30px;
                                                    font-weight: bold;
                                                "
                                            >
                                                Booking options
                                            </div>
                                            <v-row dense>
                                                <v-col cols="11">
                                                    <div
                                                        style="font-size: 18px"
                                                        class="pt-7"
                                                    >
                                                        Instant Book
                                                    </div>
                                                    <div
                                                        style="
                                                            color: grey;
                                                            font-size: 15px;
                                                        "
                                                    >
                                                        Listings you can book
                                                        without waiting for Host
                                                        approval
                                                    </div>
                                                </v-col>
                                                <v-col cols="1">
                                                    <v-switch
                                                        inset
                                                        color="black"
                                                    ></v-switch>
                                                </v-col>

                                                <v-col cols="11">
                                                    <div
                                                        style="font-size: 18px"
                                                        class="pt-3"
                                                    >
                                                        Self Check-In
                                                    </div>
                                                    <div
                                                        style="
                                                            color: grey;
                                                            font-size: 15px;
                                                        "
                                                    >
                                                        Easy access to the
                                                        property once you arrive
                                                    </div>
                                                </v-col>
                                                <v-col cols="1">
                                                    <v-switch
                                                        inset
                                                        color="black"
                                                    ></v-switch>
                                                </v-col>
                                            </v-row>
                                            <v-divider class="mt-6"></v-divider>

                                            <!-- Section 7 -->
                                            <div
                                                style="
                                                    font-size: 25px;
                                                    padding-top: 30px;
                                                    font-weight: bold;
                                                "
                                            >
                                                Accessibility Features
                                            </div>
                                            <div
                                                style="
                                                    font-size: 16px;
                                                    color: gray;
                                                "
                                            >
                                                This info was provided by the
                                                Host and reviewed by Airbnb.
                                            </div>
                                            <h4 class="mt-10">
                                                Guest entrance and parking
                                            </h4>

                                            <v-row
                                                dense
                                                justify="space-between"
                                                class="mt-1 ml-n3"
                                            >
                                                <v-col cols="6">
                                                    <v-checkbox
                                                        style="
                                                            font-size: 20px;
                                                            padding-right: 10px;
                                                        "
                                                        label="Step-free guest entrance"
                                                    ></v-checkbox>
                                                </v-col>

                                                <v-col cols="6">
                                                    <v-checkbox
                                                        style="
                                                            font-size: 20px;
                                                            padding-right: 10px;
                                                        "
                                                        label="Guest entrance wider than 32 inches"
                                                    ></v-checkbox>
                                                </v-col>
                                            </v-row>

                                            <v-row
                                                dense
                                                justify="space-between"
                                                class="mt-n8 ml-n3"
                                            >
                                                <v-col cols="6">
                                                    <v-checkbox
                                                        style="
                                                            font-size: 20px;
                                                            padding-right: 10px;
                                                        "
                                                        label="Step-free guest entrance"
                                                    ></v-checkbox>
                                                </v-col>

                                                <v-col cols="6">
                                                    <v-checkbox
                                                        style="
                                                            font-size: 20px;
                                                            padding-right: 10px;
                                                        "
                                                        label="Guest entrance wider than 32 inches"
                                                    ></v-checkbox>
                                                </v-col>
                                            </v-row>
                                            <v-divider></v-divider>

                                            <!-- Section 8 -->
                                            <div
                                                style="
                                                    font-size: 25px;
                                                    padding-top: 30px;
                                                    font-weight: bold;
                                                "
                                            >
                                                Top Tier Stays
                                            </div>
                                            <div
                                                style="font-size: 18px"
                                                class="pt-7"
                                            >
                                                Superhost
                                            </div>
                                            <div
                                                style="
                                                    color: grey;
                                                    font-size: 15px;
                                                "
                                            >
                                                Stay with recognized Hosts
                                            </div>

                                            <v-row dense>
                                                <v-col cols="11">
                                                    <a
                                                        href="#"
                                                        style="
                                                            color: black;
                                                            font-size: 16px;
                                                        "
                                                    >
                                                        Learn More</a
                                                    >
                                                </v-col>
                                                <v-col cols="1">
                                                    <v-switch
                                                        class="mt-n4"
                                                        inset
                                                        color="black"
                                                    ></v-switch>
                                                </v-col>
                                            </v-row>
                                            <v-divider></v-divider>

                                            <!-- Section 9 -->
                                            <div
                                                style="
                                                    font-size: 25px;
                                                    padding-top: 30px;
                                                    font-weight: bold;
                                                "
                                            >
                                                Host Language
                                            </div>
                                            <v-row
                                                dense
                                                justify="space-between"
                                                class="mt-1 ml-n3"
                                            >
                                                <v-col cols="6">
                                                    <v-checkbox
                                                        style="
                                                            font-size: 20px;
                                                            padding-right: 10px;
                                                        "
                                                        label="English"
                                                    ></v-checkbox>
                                                </v-col>

                                                <v-col cols="6">
                                                    <v-checkbox
                                                        style="
                                                            font-size: 20px;
                                                            padding-right: 10px;
                                                        "
                                                        label="French"
                                                    ></v-checkbox>
                                                </v-col>
                                            </v-row>

                                            <v-row
                                                dense
                                                justify="space-between"
                                                class="mt-n8 ml-n3"
                                            >
                                                <v-col cols="6">
                                                    <v-checkbox
                                                        style="
                                                            font-size: 20px;
                                                            padding-right: 10px;
                                                        "
                                                        label="German"
                                                    ></v-checkbox>
                                                </v-col>

                                                <v-col cols="6">
                                                    <v-checkbox
                                                        style="
                                                            font-size: 20px;
                                                            padding-right: 10px;
                                                        "
                                                        label="Japanese"
                                                    ></v-checkbox>
                                                </v-col>
                                            </v-row>
                                            <h3
                                                class="mb-6"
                                                style="
                                                    text-decoration: underline;
                                                    cursor: pointer;
                                                "
                                            >
                                                Show More
                                            </h3>
                                        </v-card-text>

                                        <hr />
                                        <v-card-actions
                                            variant="outlined"
                                            class="d-flex justify-space-between pa-6"
                                        >
                                            <v-btn
                                                rounded
                                                color="blue-darken-1"
                                                variant="text"
                                            >
                                                Clear All
                                            </v-btn>
                                            <v-btn
                                                style="
                                                    border-radius: 10px;
                                                    height: 50px;
                                                    width: 160px;
                                                "
                                                class="bg-grey-darken-4"
                                                variant="text"
                                                @click="dialog = false"
                                            >
                                                Show 647 stays
                                            </v-btn>
                                        </v-card-actions>
                                    </v-card>
                                </template>
                            </v-dialog>
                        </v-window-item>

                        <v-window-item value="two">
                            <v-dialog
                                transition="dialog-bottom-transition"
                                v-model="dialog"
                                scrollable
                                width="915"
                            >
                                <template v-slot:activator="{ props }">
                                    <v-btn
                                        v-bind="props"
                                        variant="outlined"
                                        width="120px"
                                        height="50px"
                                        class="mt-5"
                                        style="
                                            text-transform: capitalize;
                                            border-radius: 10px;
                                        "
                                    >
                                        <v-icon
                                            icon="mdi-swap-horizontal"
                                            style="font-size: 30px"
                                        ></v-icon>
                                        &nbsp;&nbsp; filters
                                    </v-btn>
                                </template>
                                <template v-slot:default="{ isActive }">
                                    <v-card width="900px">
                                        <v-card-title
                                            class="d-flex pa-3 text-center justify-space-around"
                                            style="font-size: 30px"
                                        >
                                            <v-btn
                                                style="
                                                    font-size: 30px;
                                                    color: red;
                                                "
                                                variant="text"
                                                @click="isActive.value = false"
                                            >
                                                <v-icon
                                                    icon="mdi-close-thick"
                                                ></v-icon>
                                            </v-btn>
                                            <h4>Filter</h4>
                                        </v-card-title>
                                        <v-divider></v-divider>

                                        <v-card-text>
                                            <!-- Section 1 -->
                                            <div
                                                style="
                                                    font-size: 25px;
                                                    padding-top: 20px;
                                                    font-weight: bold;
                                                "
                                            >
                                                Price Range
                                            </div>
                                            <div style="color: grey">
                                                The average total price for 5
                                                nights is ‎$1,229
                                            </div>

                                            <v-row
                                                dense
                                                justify="space-around"
                                                class="pt-6"
                                            >
                                                <v-col cols="5">
                                                    <small style="color: grey">
                                                        min price</small
                                                    >
                                                    <v-text-field
                                                        variant="outlined"
                                                        type="text"
                                                    >
                                                        $&nbsp;&nbsp;50
                                                    </v-text-field>
                                                </v-col>
                                                <v-col cols="2">
                                                    <h1
                                                        align="center"
                                                        class="pt-6"
                                                    >
                                                        -
                                                    </h1></v-col
                                                >
                                                <v-col cols="5">
                                                    <small style="color: grey">
                                                        max price</small
                                                    >
                                                    <v-text-field
                                                        variant="outlined"
                                                        type="text"
                                                    >
                                                        $&nbsp;&nbsp;3800+
                                                    </v-text-field>
                                                </v-col>
                                            </v-row>
                                            <v-divider></v-divider>

                                            <!-- Section 2 -->
                                            <div
                                                style="
                                                    font-size: 25px;
                                                    padding-top: 30px;
                                                    font-weight: bold;
                                                "
                                            >
                                                Type of place
                                            </div>
                                            <v-row dense justify="space-around">
                                                <v-col cols="6">
                                                    <v-list-item
                                                        title="Entire Place"
                                                        subtitle="A place all to yourself"
                                                    >
                                                        <template
                                                            v-slot:prepend
                                                        >
                                                            <v-checkbox
                                                                style="
                                                                    font-size: 20px;
                                                                    padding-right: 10px;
                                                                "
                                                                class="ml-n5"
                                                            ></v-checkbox>
                                                        </template>
                                                    </v-list-item>
                                                </v-col>

                                                <v-col cols="6">
                                                    <v-list-item
                                                        title="Private Room"
                                                        subtitle="Your own room in a home or a hotel, plus some shared common spaces"
                                                    >
                                                        <template
                                                            v-slot:prepend
                                                        >
                                                            <v-checkbox
                                                                style="
                                                                    font-size: 20px;
                                                                    padding-right: 10px;
                                                                "
                                                            ></v-checkbox>
                                                        </template>
                                                    </v-list-item>
                                                </v-col>

                                                <v-col cols="12" class="mt-n2">
                                                    <v-list-item
                                                        title="Shared Room"
                                                        subtitle="A sleeping space and common areas that may be shared with others"
                                                    >
                                                        <template
                                                            v-slot:prepend
                                                        >
                                                            <v-checkbox
                                                                style="
                                                                    font-size: 20px;
                                                                    padding-right: 10px;
                                                                "
                                                                class="ml-n5"
                                                            ></v-checkbox>
                                                        </template>
                                                    </v-list-item>
                                                </v-col>
                                            </v-row>
                                            <v-divider></v-divider>

                                            <!-- Section 3 -->
                                            <div
                                                style="
                                                    font-size: 25px;
                                                    padding-top: 30px;
                                                    font-weight: bold;
                                                "
                                            >
                                                Rooms and Beds
                                            </div>
                                            <div style="margin-top: 30px">
                                                Bedrooms
                                            </div>
                                            <v-row dense justify="space-around">
                                                <v-col cols="12" class="pt-5">
                                                    <v-btn-toggle
                                                        v-model="bedroom"
                                                        color="black"
                                                        style="gap: 10px"
                                                    >
                                                        <v-btn
                                                            value="bedroom1"
                                                            style="
                                                                border-radius: 23px;
                                                                text-transform: capitalize;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                            >Any
                                                        </v-btn>
                                                        <v-btn
                                                            value="bedroom2"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            1
                                                        </v-btn>
                                                        <v-btn
                                                            value="bedroom3"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            2
                                                        </v-btn>
                                                        <v-btn
                                                            value="bedroom4"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            3
                                                        </v-btn>
                                                        <v-btn
                                                            value="bedroom5"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            4
                                                        </v-btn>
                                                        <v-btn
                                                            value="bedroom6"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            5
                                                        </v-btn>
                                                        <v-btn
                                                            value="bedroom7"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            6
                                                        </v-btn>
                                                        <v-btn
                                                            value="bedroom8"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            7
                                                        </v-btn>
                                                        <v-btn
                                                            value="bedroom9"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            8+
                                                        </v-btn>
                                                    </v-btn-toggle>
                                                </v-col>
                                            </v-row>

                                            <div style="margin-top: 30px">
                                                Bed
                                            </div>
                                            <v-row dense justify="space-around">
                                                <v-col cols="12" class="pt-5">
                                                    <v-btn-toggle
                                                        v-model="bed"
                                                        color="black"
                                                        style="gap: 10px"
                                                    >
                                                        <v-btn
                                                            value="bed1"
                                                            style="
                                                                border-radius: 23px;
                                                                text-transform: capitalize;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                            >Any
                                                        </v-btn>
                                                        <v-btn
                                                            value="bed2"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            1
                                                        </v-btn>
                                                        <v-btn
                                                            value="bed3"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            2
                                                        </v-btn>
                                                        <v-btn
                                                            value="bed4"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            3
                                                        </v-btn>
                                                        <v-btn
                                                            value="bed5"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            4
                                                        </v-btn>
                                                        <v-btn
                                                            value="bed6"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            5
                                                        </v-btn>
                                                        <v-btn
                                                            value="bed7"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            6
                                                        </v-btn>
                                                        <v-btn
                                                            value="bed8"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            7
                                                        </v-btn>
                                                        <v-btn
                                                            value="bed9"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            8+
                                                        </v-btn>
                                                    </v-btn-toggle>
                                                </v-col>
                                            </v-row>

                                            <div style="margin-top: 30px">
                                                Bathrooms
                                            </div>
                                            <v-row dense justify="space-around">
                                                <v-col cols="12" class="pt-5">
                                                    <v-btn-toggle
                                                        v-model="bath"
                                                        color="black"
                                                        style="gap: 10px"
                                                    >
                                                        <v-btn
                                                            value="bath1"
                                                            style="
                                                                border-radius: 23px;
                                                                text-transform: capitalize;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                            >Any
                                                        </v-btn>
                                                        <v-btn
                                                            value="bath2"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            1
                                                        </v-btn>
                                                        <v-btn
                                                            value="bath3"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            2
                                                        </v-btn>
                                                        <v-btn
                                                            value="bath4"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            3
                                                        </v-btn>
                                                        <v-btn
                                                            value="bath5"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            4
                                                        </v-btn>
                                                        <v-btn
                                                            value="bath6"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            5
                                                        </v-btn>
                                                        <v-btn
                                                            value="bath7"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            6
                                                        </v-btn>
                                                        <v-btn
                                                            value="bath8"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            7
                                                        </v-btn>
                                                        <v-btn
                                                            value="bath9"
                                                            style="
                                                                border-radius: 23px;
                                                                border: 1px
                                                                    solid grey;
                                                            "
                                                        >
                                                            8+
                                                        </v-btn>
                                                    </v-btn-toggle>
                                                </v-col>
                                            </v-row>
                                            <v-divider
                                                class="mt-14"
                                            ></v-divider>

                                            <!-- Section 4 -->
                                            <div
                                                style="
                                                    font-size: 25px;
                                                    padding-top: 30px;
                                                    font-weight: bold;
                                                "
                                            >
                                                Property Type
                                            </div>
                                            <v-row
                                                dense
                                                justify="center"
                                                class="mt-5"
                                            >
                                                <v-col cols="3">
                                                    <v-btn
                                                        class="hoverbtn"
                                                        height="130"
                                                        width="170"
                                                        style="
                                                            border-radius: 15px;
                                                        "
                                                    >
                                                        <div
                                                            style="
                                                                display: flex;
                                                                flex-direction: column;
                                                                gap: 20px;
                                                                transition: 0.3s;
                                                            "
                                                        >
                                                            <v-img
                                                                width="50px"
                                                                src="https://a0.muscache.com/pictures/4d7580e1-4ab2-4d26-a3d6-97f9555ba8f9.jpg"
                                                            ></v-img>
                                                            <p>House</p>
                                                        </div>
                                                    </v-btn>
                                                </v-col>

                                                <v-col cols="3">
                                                    <v-btn
                                                        class="hoverbtn"
                                                        height="130"
                                                        width="170"
                                                        style="
                                                            border-radius: 15px;
                                                        "
                                                    >
                                                        <div
                                                            style="
                                                                display: flex;
                                                                flex-direction: column;
                                                                gap: 20px;
                                                                transition: 0.3s;
                                                            "
                                                        >
                                                            <v-img
                                                                width="50px"
                                                                src="https://a0.muscache.com/pictures/21cfc7c9-5457-494d-9779-7b0c21d81a25.jpg"
                                                            ></v-img>
                                                            <p>Apartment</p>
                                                        </div>
                                                    </v-btn>
                                                </v-col>

                                                <v-col cols="3">
                                                    <v-btn
                                                        class="hoverbtn"
                                                        height="130"
                                                        width="170"
                                                        style="
                                                            border-radius: 15px;
                                                        "
                                                    >
                                                        <div
                                                            style="
                                                                display: flex;
                                                                flex-direction: column;
                                                                gap: 20px;
                                                                transition: 0.3s;
                                                            "
                                                        >
                                                            <v-img
                                                                width="50px"
                                                                src="https://a0.muscache.com/pictures/6f261426-2e47-4c91-8b1a-7a847da2b21b.jpg"
                                                            ></v-img>
                                                            <p>Guesthouse</p>
                                                        </div>
                                                    </v-btn>
                                                </v-col>

                                                <v-col cols="3">
                                                    <v-btn
                                                        class="hoverbtn"
                                                        height="130"
                                                        width="170"
                                                        style="
                                                            border-radius: 15px;
                                                        "
                                                    >
                                                        <div
                                                            style="
                                                                display: flex;
                                                                flex-direction: column;
                                                                gap: 20px;
                                                                transition: 0.3s;
                                                            "
                                                        >
                                                            <v-img
                                                                width="50px"
                                                                src="https://a0.muscache.com/pictures/64b27fed-56a1-4f03-950a-d8da08efb428.jpg"
                                                            ></v-img>
                                                            <p>Hotel</p>
                                                        </div>
                                                    </v-btn>
                                                </v-col>
                                            </v-row>
                                            <v-divider
                                                class="mt-14"
                                            ></v-divider>

                                            <!-- Section 5 -->
                                            <div
                                                style="
                                                    font-size: 25px;
                                                    padding-top: 30px;
                                                    font-weight: bold;
                                                "
                                            >
                                                Amenities
                                            </div>
                                            <h4 class="mt-10">Essentials</h4>
                                            <v-row
                                                dense
                                                justify="space-between"
                                                class="mt-5 ml-n3"
                                            >
                                                <v-col cols="6">
                                                    <v-checkbox
                                                        style="
                                                            font-size: 20px;
                                                            padding-right: 10px;
                                                        "
                                                        label="Wifi"
                                                    ></v-checkbox>
                                                </v-col>

                                                <v-col cols="6">
                                                    <v-checkbox
                                                        style="
                                                            font-size: 20px;
                                                            padding-right: 10px;
                                                        "
                                                        label="Kitchen"
                                                    ></v-checkbox>
                                                </v-col>
                                            </v-row>

                                            <v-row
                                                dense
                                                justify="space-between"
                                                class="mt-n6 ml-n3"
                                            >
                                                <v-col cols="6">
                                                    <v-checkbox
                                                        style="
                                                            font-size: 20px;
                                                            padding-right: 10px;
                                                        "
                                                        label="Washer"
                                                    ></v-checkbox>
                                                </v-col>

                                                <v-col cols="6">
                                                    <v-checkbox
                                                        style="
                                                            font-size: 20px;
                                                            padding-right: 10px;
                                                        "
                                                        label="Dryer"
                                                    ></v-checkbox>
                                                </v-col>
                                            </v-row>

                                            <v-row
                                                dense
                                                justify="space-between"
                                                class="mt-n6 ml-n3"
                                            >
                                                <v-col cols="6">
                                                    <v-checkbox
                                                        style="
                                                            font-size: 20px;
                                                            padding-right: 10px;
                                                        "
                                                        label="Aire Conditioning"
                                                    ></v-checkbox>
                                                </v-col>

                                                <v-col cols="6">
                                                    <v-checkbox
                                                        style="
                                                            font-size: 20px;
                                                            padding-right: 10px;
                                                        "
                                                        label="Jeating"
                                                    ></v-checkbox>
                                                </v-col>
                                            </v-row>
                                            <v-divider></v-divider>

                                            <!-- Section 6 -->
                                            <div
                                                style="
                                                    font-size: 25px;
                                                    padding-top: 30px;
                                                    font-weight: bold;
                                                "
                                            >
                                                Booking options
                                            </div>
                                            <v-row dense>
                                                <v-col cols="11">
                                                    <div
                                                        style="font-size: 18px"
                                                        class="pt-7"
                                                    >
                                                        Instant Book
                                                    </div>
                                                    <div
                                                        style="
                                                            color: grey;
                                                            font-size: 15px;
                                                        "
                                                    >
                                                        Listings you can book
                                                        without waiting for Host
                                                        approval
                                                    </div>
                                                </v-col>
                                                <v-col cols="1">
                                                    <v-switch
                                                        inset
                                                        color="black"
                                                    ></v-switch>
                                                </v-col>

                                                <v-col cols="11">
                                                    <div
                                                        style="font-size: 18px"
                                                        class="pt-3"
                                                    >
                                                        Self Check-In
                                                    </div>
                                                    <div
                                                        style="
                                                            color: grey;
                                                            font-size: 15px;
                                                        "
                                                    >
                                                        Easy access to the
                                                        property once you arrive
                                                    </div>
                                                </v-col>
                                                <v-col cols="1">
                                                    <v-switch
                                                        inset
                                                        color="black"
                                                    ></v-switch>
                                                </v-col>
                                            </v-row>
                                            <v-divider class="mt-6"></v-divider>

                                            <!-- Section 7 -->
                                            <div
                                                style="
                                                    font-size: 25px;
                                                    padding-top: 30px;
                                                    font-weight: bold;
                                                "
                                            >
                                                Accessibility Features
                                            </div>
                                            <div
                                                style="
                                                    font-size: 16px;
                                                    color: gray;
                                                "
                                            >
                                                This info was provided by the
                                                Host and reviewed by Airbnb.
                                            </div>
                                            <h4 class="mt-10">
                                                Guest entrance and parking
                                            </h4>

                                            <v-row
                                                dense
                                                justify="space-between"
                                                class="mt-1 ml-n3"
                                            >
                                                <v-col cols="6">
                                                    <v-checkbox
                                                        style="
                                                            font-size: 20px;
                                                            padding-right: 10px;
                                                        "
                                                        label="Step-free guest entrance"
                                                    ></v-checkbox>
                                                </v-col>

                                                <v-col cols="6">
                                                    <v-checkbox
                                                        style="
                                                            font-size: 20px;
                                                            padding-right: 10px;
                                                        "
                                                        label="Guest entrance wider than 32 inches"
                                                    ></v-checkbox>
                                                </v-col>
                                            </v-row>

                                            <v-row
                                                dense
                                                justify="space-between"
                                                class="mt-n8 ml-n3"
                                            >
                                                <v-col cols="6">
                                                    <v-checkbox
                                                        style="
                                                            font-size: 20px;
                                                            padding-right: 10px;
                                                        "
                                                        label="Step-free guest entrance"
                                                    ></v-checkbox>
                                                </v-col>

                                                <v-col cols="6">
                                                    <v-checkbox
                                                        style="
                                                            font-size: 20px;
                                                            padding-right: 10px;
                                                        "
                                                        label="Guest entrance wider than 32 inches"
                                                    ></v-checkbox>
                                                </v-col>
                                            </v-row>
                                            <v-divider></v-divider>

                                            <!-- Section 8 -->
                                            <div
                                                style="
                                                    font-size: 25px;
                                                    padding-top: 30px;
                                                    font-weight: bold;
                                                "
                                            >
                                                Top Tier Stays
                                            </div>
                                            <div
                                                style="font-size: 18px"
                                                class="pt-7"
                                            >
                                                Superhost
                                            </div>
                                            <div
                                                style="
                                                    color: grey;
                                                    font-size: 15px;
                                                "
                                            >
                                                Stay with recognized Hosts
                                            </div>

                                            <v-row dense>
                                                <v-col cols="11">
                                                    <a
                                                        href="#"
                                                        style="
                                                            color: black;
                                                            font-size: 16px;
                                                        "
                                                    >
                                                        Learn More</a
                                                    >
                                                </v-col>
                                                <v-col cols="1">
                                                    <v-switch
                                                        class="mt-n4"
                                                        inset
                                                        color="black"
                                                    ></v-switch>
                                                </v-col>
                                            </v-row>
                                            <v-divider></v-divider>

                                            <!-- Section 9 -->
                                            <div
                                                style="
                                                    font-size: 25px;
                                                    padding-top: 30px;
                                                    font-weight: bold;
                                                "
                                            >
                                                Host Language
                                            </div>
                                            <v-row
                                                dense
                                                justify="space-between"
                                                class="mt-1 ml-n3"
                                            >
                                                <v-col cols="6">
                                                    <v-checkbox
                                                        style="
                                                            font-size: 20px;
                                                            padding-right: 10px;
                                                        "
                                                        label="English"
                                                    ></v-checkbox>
                                                </v-col>

                                                <v-col cols="6">
                                                    <v-checkbox
                                                        style="
                                                            font-size: 20px;
                                                            padding-right: 10px;
                                                        "
                                                        label="French"
                                                    ></v-checkbox>
                                                </v-col>
                                            </v-row>

                                            <v-row
                                                dense
                                                justify="space-between"
                                                class="mt-n8 ml-n3"
                                            >
                                                <v-col cols="6">
                                                    <v-checkbox
                                                        style="
                                                            font-size: 20px;
                                                            padding-right: 10px;
                                                        "
                                                        label="German"
                                                    ></v-checkbox>
                                                </v-col>

                                                <v-col cols="6">
                                                    <v-checkbox
                                                        style="
                                                            font-size: 20px;
                                                            padding-right: 10px;
                                                        "
                                                        label="Japanese"
                                                    ></v-checkbox>
                                                </v-col>
                                            </v-row>
                                            <h3
                                                class="mb-6"
                                                style="
                                                    text-decoration: underline;
                                                    cursor: pointer;
                                                "
                                            >
                                                Show More
                                            </h3>
                                        </v-card-text>

                                        <hr />
                                        <v-card-actions
                                            variant="outlined"
                                            class="d-flex justify-space-between pa-6"
                                        >
                                            <v-btn
                                                rounded
                                                color="blue-darken-1"
                                                variant="text"
                                            >
                                                Clear All
                                            </v-btn>
                                            <v-btn
                                                style="
                                                    border-radius: 10px;
                                                    height: 50px;
                                                    width: 160px;
                                                "
                                                class="bg-grey-darken-4"
                                                variant="text"
                                                @click="dialog = false"
                                            >
                                                Show 647 stays
                                            </v-btn>
                                        </v-card-actions>
                                    </v-card>
                                </template>
                            </v-dialog>
                        </v-window-item>
                    </v-window>
                </v-col>
            </v-row>
        </v-container>
    </v-app-bar>

    <v-container>
        <v-row justify="center" class="mt-5">
            <v-card
                width="550"
                style="
                    border-radius: 10px;
                    display: flex;
                    justify-content: space-between;
                "
                elevation="3"
            >
                <div style="display: flex; gap: 5px; padding: 15px 0px">
                    <h4 class="btn-area" style="border-color: grey">
                        Display total price
                    </h4>
                    <div class="btn-area">Includes all fees, before taxes</div>
                </div>
                <v-switch
                    class="mt-2"
                    v-model="model"
                    hide-details
                    inset
                    color="black"
                ></v-switch>
            </v-card>
        </v-row>
    </v-container>

    <v-window v-model="tab">
        <v-window-item value="one">
            <v-container>
                <v-row justify="center" class="mt-4">
                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>
                </v-row>

                <v-row justify="center" class="mt-4">
                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>
                </v-row>

                <v-row justify="center" class="mt-4">
                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>
                </v-row>

                <v-row justify="center" class="mt-4">
                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>
                </v-row>

                <v-row justify="center" class="mt-4">
                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>
                </v-row>
            </v-container>
        </v-window-item>

        <v-window-item value="two">
            <v-container>
                <v-row justify="center" class="mt-4">
                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>
                </v-row>

                <v-row justify="center" class="mt-4">
                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>
                </v-row>

                <v-row justify="center" class="mt-4">
                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>
                </v-row>

                <v-row justify="center" class="mt-4">
                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>
                </v-row>

                <v-row justify="center" class="mt-4">
                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>

                    <v-col cols="2">
                        <v-carousel
                            cycle
                            height="300"
                            style="border-radius: 15px"
                            hide-delimiters
                            show-arrows="hover"
                        >
                            <v-carousel-item
                                v-for="(slide, i) in slideimg"
                                :key="i"
                            >
                                <v-sheet
                                    class="d-flex justify-center"
                                    height="100%"
                                    width="100%"
                                >
                                    <img :src="slide" />
                                </v-sheet>
                            </v-carousel-item>
                        </v-carousel>
                        <h4 class="mt-4">Thanh Hoa, Vietnam</h4>
                        <div>992 Kilometers away</div>
                        <div>5 nights, Apr 13 - 18</div>
                        <a href="#"> $747 total before taxes</a>
                    </v-col>
                </v-row>
            </v-container>
        </v-window-item>
    </v-window>
</template>



<script>
    export default {
        data: () => ({
            threechoice: ["Anywhere", "Any Week", "Add Quests"],
            onboarding: 0,
            length: 3,
            tab: null,
            model: null,

            slideimg: [
                "https://a0.muscache.com/im/pictures/0adc1aec-bd6f-4f10-8536-a3bb6faecd20.jpg?im_w=720",
                "https://a0.muscache.com/im/pictures/a3333097-d82d-4146-b583-7297523b8a78.jpg?im_w=720",
                "https://a0.muscache.com/im/pictures/9c38bfea-2bab-4bfa-9ff0-d4b5bdd9db45.jpg?im_w=720",
                "https://a0.muscache.com/im/pictures/44ab02d3-376f-4fe6-bb2c-108497f47a64.jpg?im_w=720",
                "https://a0.muscache.com/im/pictures/246b0fda-97a8-4fb0-ae13-98cbe719f3aa.jpg?im_w=720",
                "https://a0.muscache.com/im/pictures/050adcbf-01a1-4de8-9e7c-f35bb7e582d5.jpg?im_w=720",
                "https://a0.muscache.com/im/pictures/c5283ef4-539f-42f2-96a9-70ddd2f1d8c2.jpg?im_w=720",
                "https://a0.muscache.com/im/pictures/52aff2f9-c57e-45e8-8db7-e609ed402c33.jpg?im_w=720",
                "https://a0.muscache.com/im/pictures/cd520423-4f47-4088-86c8-99686622cf09.jpg?im_w=720",
                "https://a0.muscache.com/im/pictures/2515d542-3554-4ffa-8735-e95321caaf1f.jpg?im_w=720",
                "https://a0.muscache.com/im/pictures/c637c024-29ed-41d7-b68b-3ec5bf3d64e6.jpg?im_w=720",
                "https://a0.muscache.com/im/pictures/247bacd9-d90a-4086-86fa-2080c4c69d4f.jpg?im_w=720",
                "https://a0.muscache.com/im/pictures/7af11fc5-ba53-4bc4-817b-d436843b9da0.jpg?im_w=720",
                "https://a0.muscache.com/im/pictures/miso/Hosting-569847255286350963/original/0854a3a7-44b7-425f-8a25-281ad354156d.jpeg?im_w=720",
                "https://a0.muscache.com/im/pictures/5643acf3-3200-473e-aa8c-e827a8677465.jpg?im_w=720",
            ],

            items1: [{ title: "Sign Up" }, { title: "Log In" }],

            items2: [
                { title: "Airbnb your home" },
                { title: "Host an Experience" },
                { title: "help" },
            ],

            colors: [
                "indigo",
                "warning",
                "pink darken-2",
                "red lighten-1",
                "deep-purple accent-4",
            ],
            slides: ["First", "Second", "Third", "Fourth", "Fifth"],

            dialog: false,
            bedroom: "bedroom1",
            bed: "bed1",
            bath: "bath1",
            model: true,
        }),
    };
</script>


<style scoped>
.btn-area {
    display: flex;
    justify-content: center;
    padding: 8px 30px;
    gap: 30px;
    text-transform: capitalize;
    border: 1px solid;
    border-bottom: 0;
    border-left: 0;
    border-top: 0;
    height: 30px;
}

.btn-area:last-child {
    border-right: 0;
    color: grey;
}

.tabstyle {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 5px;
    text-transform: capitalize;
}

.slidebox {
    background-color: red;
    height: 300px;
    width: 300px;
    margin-top: 200px;
    border-radius: 25px;
}
.hoverbtn:hover {
    border: 1px solid black;
    transition: 0.5s;
    transform: scale(0.9);
}
</style>