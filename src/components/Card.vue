<template>
    <v-card>
        <div class="container">
            <div class="div-img">
                <img src="https://cdn.ocp.news/2019/07/jaragua-do-sul-tera-evento-com-seis-bandas-no-dia-mundial-do-rock.jpg" alt="imagem do evento" class="img-event">
            </div>
            <div class="information">
                <h3>Show não existe amor em SP</h3>
                <p>04/10/2021 - 19h</p>
                <p>Show de rock com várias bandas independentes</p>
                <p>Av. Paulista, 345</p>
                <h4> 50 Participantes</h4>
            </div>
            <Button  buttonName="Participar" class="btn-event"/>
        </div>
    </v-card>
</template>

<script>
    import Button from './Button.vue'
export default {
    components: { Button }
}
</script>

<style>
    .container {
        width: 100%;
        height: 200px;
        display: flex;
        align-items: center;
        justify-content: flex-start;        

    }

    .img-event {
        height: 118px;
        width: 177px; 
        border-radius: 8px;       
    }
    .div-img {
        margin-right: 20px;
    }
    .information p {
        margin-bottom: 5px !important;
        color: #5B5858;
    }
    .btn-event {
        margin-top: 100px;
    }
</style>