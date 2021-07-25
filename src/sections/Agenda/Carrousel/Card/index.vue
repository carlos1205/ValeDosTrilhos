<template>
    <div>
        <b-card
            no-body
            style="max-width: 20rem;"
            img-src="https://placekitten.com/380/200"
            img-alt="Image"
            img-top
        >
            <b-card-body>
                <b-row>
                    <b-col cols="3">
                        <p class="text-light fs-6 date">
                            <span>
                                09
                            </span>
                            <span>
                                JUL
                            </span>
                        </p>
                    </b-col>
                    <b-col cols="9">
                        <h3 class="fs-5">
                            Semana Empreendedora
                        </h3>
                    </b-col>
                </b-row>
            </b-card-body>

            <b-card-footer>
                <b-button href="#" variant="outline-secondary" >Ver Mais</b-button>
            </b-card-footer>
        </b-card>
    </div>
</template>

<style scoped>
    span {
        font-weight: bolder;
    }
    .card { 
        background-color: rgba(255, 255, 255, .5);
    }
    .card .date {
        background-color: #ffcb05;
        margin-bottom: 0;
        border-radius: 0.3rem;
        padding-left: .5rem;
    }
    .card-footer {
        text-align: end;
    }
</style>