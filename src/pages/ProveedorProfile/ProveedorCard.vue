<template>
    <div class="content">
        <div class="md-layout">
            <div 
            class="md-layout-item md-large-size-100 md-xsmall-size-100 md-size-50">
                <nav-tabs-card>
                    <template slot="content">
                        <span class="md-nav-tabs-title">Acción:</span>
                        <md-tabs class="md-success" md-alignment="left">
                            <md-tab id="tab-home" md-label="Proveedor" md-icon="bug_report">
                                <form>
                                    <md-card>
                                        <md-card-header
                                        :data-background-color="dataBackgroundColor">
                                            <h4 class="tittle">Editar proveedores</h4>
                                            <p class="category">Datos del Proveedor</p>
                                        </md-card-header>
                                        <md-card-content>
                                            <div class="md-layout lg-layout">
                                                <div class="md-layout-item md-small-size-100 md-size-33">
                                                    <md-field>
                                                        <label>R.F.C.:</label>
                                                        <md-input v-model="rfc"></md-input>
                                                    </md-field>
                                                </div>
                                                <div
                                                class="md-layout-item md-small-size-100 md-size-33">
                                                    <md-field>
                                                        <label>Razón social:</label>
                                                        <md-input v-model="razonsocial"></md-input>
                                                    </md-field>
                                                </div>
                                                <div
                                                class="md-layout-item md-small-size-100 md-size-33">
                                                    <md-field>
                                                        <label>Nombre de Contacto:</label>
                                                        <md-input v-model="nombrecontacto"></md-input>
                                                    </md-field>
                                                </div>
                                            </div>
                                            <div class="md-layout lg-layout">
                                                <div class="md-layout-item md-small-size-100 md-size-33">
                                                    <md-field>
                                                        <label>Calle:</label>
                                                        <md-input v-model="calle"></md-input>
                                                    </md-field>
                                                </div>
                                                <div class="md-layout-item md-small-size-100 md-size-33">
                                                    <md-field>
                                                        <label>No. Inteior:</label>
                                                        <md-input v-model="numinterior"></md-input>
                                                    </md-field>
                                                </div>
                                                <div class="md-layout-item md-small-size-100 md-size-33">
                                                    <md-field>
                                                        <label>No. Exteior:</label>
                                                        <md-input v-model="numexterior"></md-input>
                                                    </md-field>
                                                </div>
                                                <div class="md-layout-item md-small-size-100 md-size-33">
                                                    <md-field>
                                                        <md-select
                                                        v-model="country"
                                                        name="country"
                                                        id="country"
                                                        placeholder="Colonia">
                                                            <md-option value="australia">Noxtongo</md-option>
                                                            <md-option value="brazil">Tlaxinacalpan</md-option>
                                                            <md-option value="japan">Japan</md-option>
                                                            <md-option value="united-states">United States</md-option>
                                                        </md-select>
                                                    </md-field>
                                                </div>
                                                <div class="md-layout-item md-small-size-100 md-size-33">
                                                    <md-field>
                                                        <label>Localidad/Delegación:</label>
                                                        <md-input v-model="localidad"></md-input>
                                                    </md-field>
                                                </div>
                                                <div class="md-layout-item md-small-size-100 md-size-33">
                                                    <md-field>
                                                        <!--<label>Entidad:</label>
                                                        <md-input v-model="entidad"></md-input>-->
                                                        <md-select
                                                        v-model="entidades"
                                                        name="entidades"
                                                        id="entidades"
                                                        placeholder="Estados">
                                                            <md-option v-for="entitie in entidades"
                                                            v-bind:key="entitie.id"
                                                            v-bind:value="entitie.strValor"
                                                            >{{ entitie.strValor }}</md-option>
                                                        </md-select>
                                                    </md-field>
                                                </div>
                                                <div class="md-layout-item md-small-size-100 md-size-33">
                                                    <md-field>
                                                        <label>Municipio:</label>
                                                        <md-input v-model="municipio"></md-input>
                                                    </md-field>
                                                </div>
                                                <div class="md-layout-item md-small-size-100 md-size-33">
                                                    <md-field>
                                                        <label>Pais:</label>
                                                        <md-input v-model="pais"></md-input>
                                                    </md-field>
                                                </div>
                                                <div class="md-layout-item md-small-size-100 md-size-33">
                                                    <md-field>
                                                        <label>Codigo Postal:</label>
                                                        <md-input v-model="codigopostal"></md-input>
                                                    </md-field>
                                                </div>
                                                <div class="md-layout-item md-small-size-100 md-size-33">
                                                    <md-field>
                                                        <label>email:</label>
                                                        <md-input v-model="email"></md-input>
                                                    </md-field>
                                                </div>
                                                <div class="md-layout-item md-small-size-100 md-size-33">
                                                    <md-field>
                                                        <label>Telefono:</label>
                                                        <md-input v-model="telefono"></md-input>
                                                    </md-field>
                                                </div>
                                                <div class="md-layout-item md-small-size-100 md-size-33">
                                                    <md-field>
                                                        <label>Status:</label>
                                                        <md-input v-model="status"></md-input>
                                                    </md-field>
                                                </div>
                                                <div class="md-layout-item md-small-size-100 md-size-33">
                                                    <md-button class="md-raised md-success">Registrar</md-button>
                                                </div>
                                            </div>
                                        </md-card-content>
                                    </md-card>
                                </form>
                            </md-tab>
                            <md-tab id="tab-pages" md-label="Buscar" md-icon="code">
                                <nav-tabs-table></nav-tabs-table>
                            </md-tab>
                        </md-tabs>
                    </template>
                </nav-tabs-card>
            </div>
        </div>
    </div>
</template>
<script>
import { NavTabsCard, NavTabsTable } from "@/components";
//import axios from "axios";

export default {
    components: {
        NavTabsCard,
        NavTabsTable,
    },
    name: "edit-profile-form",
    props: {
        dataBackgroundColor: {
            type: String,
            default: "",
        },
    },
    data() {
        return{
            username: "",
            rfc: "",
            razonsocial: "",
            nombrecontacto: "",
            calle: "",
            numinterior: "",
            numexterior: "",
            colonia: "",
            localidad: "",
            entidad: "",
            municipio: "",
            pais: "",
            codigopostal: null,
            email: "",
            telefono: null,
            status: "",
            entidades: [],
        };
    },
    methods: {
        getEstados() {
            this.$http
            .get("ruta")
            .them((response) => {
                this.entidades = response.data;
                console.log(this.entidades.length);
            })
            .catch((error) => console.log(error));
        },
    },
};
</script>
<style>

</style>