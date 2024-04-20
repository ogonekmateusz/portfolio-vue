<template>
        <div class="ideas">
            <div class="rectangle"></div>
            <div class="ideas-block">
                <div class="ideas-block-wrapper">    
                    <h1>Have any project in mind?</h1>
                    <p>Feel free to contant me or just say friendly hello!</p>
                </div>
                <div class="ideas-block-emailButton">
                     <EmailMe></EmailMe>
                </div>
            </div>
        </div>
</template>

<script setup lang="ts">
import EmailMe from "../EmailMe.vue";
</script>

<style scoped>
.ideas{
    display: flex;
    align-items: center;
    .rectangle{
        width: 10px;
        background-color: var(--primary);
        height: 213px;
    }   
    .ideas-block{
        width: 81%;
        display: flex;
        .ideas-block-wrapper{
            width:40% ;
            display: flex;
            flex-direction: column;
        }
        h1{
            color:white;
            font-size: 38px;
        }
        p{
            font-size: 16px; 
            color: var(--gray); 
        }
    }
}

</style>