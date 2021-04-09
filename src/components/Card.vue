<template>
    <div style="margin-top: 10px;">
        <b-col>
            <b-card :title="nome" 
                    style="max-width:20rem"
                    class="mb-2"
                    border-variant="primary"
                    header-bg-variant="primary"
                    header-text-variant="white"
                    align="center"
                    :img-src="linkimg"
                    img-alt="Image"
                    img-top
                    tag="article"
                    >
                <b-card-text>{{descricao}}</b-card-text>
                <b-button variant="primary">Comprar</b-button>
            </b-card>
        </b-col>     
    </div>
</template>

<script>
export default {
    props: {
        nome:{
            type: String,
            require: true,
        },
        linkimg:{
            type: String,
            require: true,
        },
        descricao:{
            type: String,
            require: true,
        }
    }
}
</script>
