<template>
    <div class="ui centered card">
        <!-- bill shown when we are not in editing mode -->
            <div class="content" v-show="!isEditing">
                <div class="header">
                    {{ bill.title }}
                </div>
                <div class="meta">
                    {{ bill.value }}
                </div>
                <div class="extra content">
                    <span class="right floated edit icon" @click="showForm">
                        <i class="edit icon"></i>
                    </span>
                </div>
            </div>
            <!-- form is visible when we are in editing mode -->
            <div class="content" v-show="isEditing">
                <div class="ui form">
                    <div class="field">
                        <label>Title</label>
                        <input type="text" v-model="bill.title" >
                    </div>
                    <div class="field">
                        <label>Value</label>
                        <input type="text" v-model="bill.value">
                    </div>
                    <div class="ui two button attached buttons">
                        <button class="ui basic blue button" @click="hideForm">
                            Close X
                        </button>
                    </div>
                </div>
            </div>
            <div class="ui bottom attached green basic button" v-show="bill.paid" @click="changeStatus()">
                Paid
            </div>
            <div class="ui bottom attached red basic button" v-show="!bill.paid">
                Due
            </div>
        </div>

</template>    

<script>
export default {
    props: ['bill'],
    data(){
        return {
            isEditing: false,
        };
    },
    methods: {
        showForm(){
            this.isEditing = true;
        },
        hideForm(){
            this.isEditing = false;
        },
    },
};
</script>
