<script setup>
import { ref } from 'vue';
import { Inertia } from '@inertiajs/inertia';
import { Head, Link } from '@inertiajs/inertia-vue3';
import JetApplicationMark from '@/Jetstream/ApplicationMark.vue';
import JetBanner from '@/Jetstream/Banner.vue';
import JetDropdown from '@/Jetstream/Dropdown.vue';
import JetDropdownLink from '@/Jetstream/DropdownLink.vue';
import JetNavLink from '@/Jetstream/NavLink.vue';
import JetResponsiveNavLink from '@/Jetstream/ResponsiveNavLink.vue';

defineProps({
    title: String,
});

const showingNavigationDropdown = ref(false);

const logout = () => {
    Inertia.post(route('logout'));
};
</script>

<template>

    <div class="wrapper">

      <nav class="main-header navbar navbar-expand navbar-white navbar-light">
        <!-- Left navbar links -->
        <ul class="navbar-nav">
            <li class="nav-item">
                <a class="nav-link" data-widget="pushmenu" href="#" role="button"><i class="fas fa-bars"></i></a>
            </li>
        </ul>
        <!-- Right navbar links -->
        <ul class="navbar-nav ml-auto">
            <!-- Messages Dropdown Menu -->
            <li class="nav-item d-none d-sm-inline-block">
                <a href="Logout.php" class="nav-link">Log Out</a>
            </li>
        </ul>
    </nav>

  <aside class="main-sidebar sidebar-dark-primary elevation-4">
    <!-- Brand Logo -->
    <a href="index3.html" class="brand-link">
        <img src="dist/img/AdminLTELogo.png" alt="AdminLTE Logo" class="brand-image img-circle elevation-3">
        <span class="brand-text font-weight-light">BEJ Online</span>
    </a>
    <!-- Sidebar -->
    <div class="sidebar os-host os-theme-light os-host-resize-disabled os-host-scrollbar-horizontal-hidden os-host-transition os-host-overflow os-host-overflow-y"><div class="os-resize-observer-host observed"><div class="os-resize-observer" style="left: 0px; right: auto;"></div></div><div class="os-size-auto-observer observed" style="height: calc(100% + 1px); float: left;"><div class="os-resize-observer"></div></div><div class="os-content-glue" style="margin: 0px -8px; width: 249px; height: 508px;"></div><div class="os-padding"><div class="os-viewport os-viewport-native-scrollbars-invisible" style="overflow-y: scroll;"><div class="os-content" style="padding: 0px 8px; height: 100%; width: 100%;">
        <div class="user-panel mt-3 pb-3 mb-3 d-flex">
            <div class="image">
                
            </div>
            <div class="info">
                <a :href="route('profile.show')">
                                            Profile
                                        </a>
            </div>
        </div>
        <nav class="mt-2">
            <ul class="nav nav-pills nav-sidebar flex-column" data-widget="treeview" role="menu" data-accordion="false">
                <li class="nav-item has-treeview menu-open">
                    <a href="#" class="nav-link active">
                        <i class="far fa-circle nav-icon"></i><p>Vizualizare Generala<i class="right fas fa-angle-left"></i></p>
                    </a>
                    <ul class="nav nav-treeview">
                        <li class="nav-item">
                            <a class="nav-link active" href="DosareDeschise.php"><i class="far fa-circle nav-icon"></i><p>Dosare Deschise</p></a> 
                        </li>
                        <li class="nav-item">
                            <a class="nav-link " href="DosareInchise.php"><i class="far fa-circle nav-icon"></i><p>Dosare Inchise</p></a>
                        </li>
                    </ul>
                </li>
                <li class="nav-item has-treeview ">
                    <a href="#" class="nav-link ">
                        <i class="far fa-circle nav-icon"></i><p>Inregistrari Dosare<i class="right fas fa-angle-left"></i></p>
                    </a>
                    <ul class="nav nav-treeview">
                        <li class="nav-item">
                            <a class="nav-link " href="InregDosar.php"><i class="far fa-circle nav-icon"></i><p>LEI</p></a> 
                        </li>
                        <li class="nav-item">
                            <a class="nav-link " href="InregDosarValuta.php"><i class="far fa-circle nav-icon"></i><p>Valuta</p></a>
                        </li>
                    </ul>
                </li>
                <li class="nav-item has-treeview ">
                    <a href="#" class="nav-link ">
                        <i class="far fa-circle nav-icon"></i><p>Operatiuni Dosare<i class="right fas fa-angle-left"></i></p>
                    </a>
                    <ul class="nav nav-treeview">
                        <li class="nav-item">
                            <a class="nav-link " href="ModDosar.php"><i class="far fa-circle nav-icon"></i><p>Modificare Dosare Lei</p></a> 
                        </li>
                        <li class="nav-item">
                            <a class="nav-link " href="ModDosarValuta.php"><i class="far fa-circle nav-icon"></i><p>Modificare Dosare Valuta</p></a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link " href="Delete.php"><i class="far fa-circle nav-icon"></i><p>Stergere Dosare</p></a>
                        </li>
                    </ul>
                </li>
                <li class="nav-item has-treeview ">
                    <a href="#" class="nav-link ">
                        <i class="far fa-circle nav-icon"></i><p>Operatiuni Documente<i class="right fas fa-angle-left"></i></p>
                    </a>
                    <ul class="nav nav-treeview">
                        <li class="nav-item">
                            <a class="nav-link " href="Upload.php"><i class="far fa-circle nav-icon"></i><p>Incarcare Documente</p></a> 
                        </li>
                        <li class="nav-item">
                            <a class="nav-link " href="DeleteDoc.php"><i class="far fa-circle nav-icon"></i><p>Stergere Documente</p></a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link " href="UploadIncuviintare.php"><i class="far fa-circle nav-icon"></i><p>Incarcare Incuviintare</p></a>
                        </li>
                    </ul>
                </li>
                <li class="nav-item has-treeview ">
                    <a href="#" class="nav-link ">
                        <i class="far fa-circle nav-icon"></i><p>Operatiuni ANAF<i class="right fas fa-angle-left"></i></p>
                    </a>
                    <ul class="nav nav-treeview">
                        <li class="nav-item">
                            <a class="nav-link " href="EmitereInterogari.php"><i class="far fa-circle nav-icon"></i><p>Interogare</p></a> 
                        </li>
                        <li class="nav-item">
                            <a class="nav-link " href="InregAngajatori.php"><i class="far fa-circle nav-icon"></i><p>Inregistrare Manuala Angajatori/Conturi</p></a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link " href="ANAFAngajatori.php"><i class="far fa-circle nav-icon"></i><p>Import Fisier Angajatori</p></a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link " href="ANAFBanci.php"><i class="far fa-circle nav-icon"></i><p>Import Fisier Conturi Bancare</p></a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link " href="PrintRaspAng1.php"><i class="far fa-circle nav-icon"></i><p>Print Raspuns Angajatori</p></a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link " href="PrintRaspConturi1.php"><i class="far fa-circle nav-icon"></i><p>Print Raspuns Conturi</p></a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link " href="DeleteConturiAngajatori.php"><i class="far fa-circle nav-icon"></i><p>Stergere Conturi/Angajatori</p></a>
                        </li>
                    </ul>
                </li>

                <li class="nav-item ">
                    <a href="#" class="nav-link ">
                        <i class="nav-icon far fa-plus-square"></i>
                        <p>Template<i class="fas fa-angle-left right"></i></p>
                    </a>
                    <ul class="nav nav-treeview" style="display: none; ">
                        <li class="nav-item">
                            <a href="PrimulLot.php" class="nav-link ">
                                <i class="far fa-circle nav-icon"></i>
                                <p>Primul Lot</p>
                            </a>
                        </li>
                        <li class="nav-item ">
                            <a href="#" class="nav-link">
                                <i class="far fa-circle nav-icon"></i>
                                <p>
                                    Solicitari Informatii
                                    <i class="fas fa-angle-left right"></i>
                                </p>
                            </a>
                            <ul class="nav nav-treeview" style="display: none; ">
                                <li class="nav-item">
                                    <a href="AdresaCnpas1.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Adresa CNPAS</p>
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a href="ITM1.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Adresa ITM</p>
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a href="AdresaPrimarie1.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Adresa Primarie</p>
                                    </a>
                                </li>
                            </ul>
                        </li>
                        <li class="nav-item ">
                            <a href="#" class="nav-link">
                                <i class="far fa-circle nav-icon"></i>
                                <p>
                                    Popriri
                                    <i class="fas fa-angle-left right"></i>
                                </p>
                            </a>
                            <ul class="nav nav-treeview" style="display: none;">
                                <li class="nav-item">
                                    <a href="PoprireSalariu1.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Poprire Angajatori Cu Doc. Anexe Fara Incuviintari</p>
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a href="PoprireSalariuIncunv.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Poprire Angajatori Cu Doc. Anexe + Incuviintari</p>
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a href="PoprireSalariuSimplu1.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Poprire Angajatori Fara Doc. Anexe</p>
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a href="InstPopAng1.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Instiintare Poprire Angajator</p>
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a href="BanciTemp.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Poprire Conturi Cu Doc. Anexe Fara Incuviintari</p>
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a href="BanciTempIncunv.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Poprire Conturi Cu Doc. Anexe + Incuviintari</p>
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a href="BanciTempSimplu1.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Poprire Conturi Fara Doc. Anexe</p>
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a href="InstPopBanca1.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Instiintare Poprire Banca</p>
                                    </a>
                                </li>
                            </ul>
                        </li>
                        <li class="nav-item ">
                            <a href="#" class="nav-link">
                                <i class="far fa-circle nav-icon"></i>
                                <p>
                                    Sistari
                                    <i class="fas fa-angle-left right"></i>
                                </p>
                            </a>
                            <ul class="nav nav-treeview" style="display: none;">
                                <li class="nav-item">
                                    <a href="SistareBanci1.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Sistare Banci</p>
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a href="SistareAngajator1.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Sistare Angajator</p>
                                    </a>
                                </li>
                            </ul>
                        </li>
                        <li class="nav-item ">
                            <a href="#" class="nav-link">
                                <i class="far fa-circle nav-icon"></i>
                                <p>
                                    Dosar
                                    <i class="fas fa-angle-left right"></i>
                                </p>
                            </a>
                            <ul class="nav nav-treeview" style="display: none;">
                                <li class="nav-item">
                                    <a href="Incuviintare1.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Cerere Incuviintare</p>
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a href="IncheiereChelt1.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Incheiere Cheltuieli</p>
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a href="SomatieMob1.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Somatie Mobiliara</p>
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a href="SomatieImo1.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Somatie Imobiliara</p>
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a href="SomatieCambiala1.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Somatie Cambiala</p>
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a href="ElibSume1.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Incheiere Eliberare Sume</p>
                                    </a>
                                </li>
                            </ul>
                        </li>
                        <li class="nav-item ">
                            <a href="#" class="nav-link">
                                <i class="far fa-circle nav-icon"></i>
                                <p>
                                    Incetare Executare
                                    <i class="fas fa-angle-left right"></i>
                                </p>
                            </a>
                            <ul class="nav nav-treeview" style="display: none;">
                                <li class="nav-item">
                                    <a href="IncheiereExecutare1.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Incheiere Executare</p>
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a href="AnulareExecutare1.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Anulare Executare</p>
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a href="IncuviintareRespinsa1.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Incuviintare Respinsa</p>
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a href="DesfiintareTitlu1.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Desfiintare Titlu Executoriu</p>
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a href="IncheiereIncetareCreditor1.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Incetare Cerere Creditor</p>
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a href="InvsolvDec1.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Insolvabilitate Decedat</p>
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a href="IncetareInsolv1.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Insolvabilitate</p>
                                    </a>
                                </li>
                            </ul>
                        </li>
                        <li class="nav-item ">
                            <a href="#" class="nav-link">
                                <i class="far fa-circle nav-icon"></i>
                                <p>
                                    Bunuri Mobile
                                    <i class="fas fa-angle-left right"></i>
                                </p>
                            </a>
                            <ul class="nav nav-treeview" style="display: none; ">
                                <li class="nav-item">
                                    <a href="AdresaServRutierSechestru1.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Adresa PV Sechestru</p>
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a href="SechestruAuto1.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>PV Sechestru Auto</p>
                                    </a>
                                </li>
                            </ul>
                        </li>
                        <li class="nav-item">
                            <a href="#" class="nav-link">
                                <i class="far fa-circle nav-icon"></i>
                                <p>
                                    Bunuri Imobile
                                    <i class="fas fa-angle-left right"></i>
                                </p>
                            </a>
                            <ul class="nav nav-treeview">
                                <li class="nav-item">
                                    <a href="#" class="nav-link">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>...</p>
                                    </a>
                                </li>
                            </ul>
                        </li>
                        <li class="nav-item ">
                            <a href="#" class="nav-link">
                                <i class="far fa-circle nav-icon"></i>
                                <p>
                                    Dovada Comunicare
                                    <i class="fas fa-angle-left right"></i>
                                </p>
                            </a>
                            <ul class="nav nav-treeview" style="display: none; ">
                                <li class="nav-item">
                                    <a href="DovadaComunicare1.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Dovada Comunicare</p>
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a href="DovadaComunicareITM1.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Dovada Comunicare ITM</p>
                                    </a>
                                </li>
                                <li class="nav-item">
                                    <a href="DovadaComunicarePrimarie1.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Dovada Comunicare Primarie</p>
                                    </a>
                                </li>
                            </ul>
                        </li>
                        <li class="nav-item ">
                            <a href="#" class="nav-link">
                                <i class="far fa-circle nav-icon"></i>
                                <p>
                                    Plic
                                    <i class="fas fa-angle-left right"></i>
                                </p>
                            </a>
                            <ul class="nav nav-treeview" style="display: none; ">
                                <li class="nav-item">
                                    <a href="Plic1.php" class="nav-link ">
                                        <i class="far fa-circle nav-icon"></i>
                                        <p>Print Plic</p>
                                    </a>
                                </li>
                            </ul>
                        </li>
                    </ul>
                </li>
                <li class="nav-item has-treeview ">
                    <a href="#" class="nav-link ">
                        <i class="far fa-circle nav-icon"></i><p>Bunuri<i class="right fas fa-angle-left"></i></p>
                    </a>
                    <ul class="nav nav-treeview">
                        <li class="nav-item">
                            <a class="nav-link " href="ViewBunuri.php"><i class="far fa-circle nav-icon"></i><p>Vizualizare Bunuri</p></a> 
                        </li>
                        <li class="nav-item">
                            <a class="nav-link " href="InregBunuri.php"><i class="far fa-circle nav-icon"></i><p>Inregistrare Bunuri Mobile</p></a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link " href="InregBunuriImobile.php"><i class="far fa-circle nav-icon"></i><p>Inregistrare Bunuri Imobile</p></a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link " href="EditareBunuri.php"><i class="far fa-circle nav-icon"></i><p>Modificare Bunuri</p></a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link " href="DeleteBunuri.php"><i class="far fa-circle nav-icon"></i><p>Stergere Bunuri</p></a>
                        </li>
                    </ul>
                </li>
                <li class="nav-item has- ">
                    <a href="#" class="nav-link ">
                        <i class="far fa-circle nav-icon"></i><p>Incasari<i class="right fas fa-angle-left"></i></p>
                    </a>
                    <ul class="nav nav-treeview">
                        <li class="nav-item">
                            <a class="nav-link " href="Facturi1.php"><i class="far fa-circle nav-icon"></i><p>Facturi</p></a> 
                        </li>
                        <li class="nav-item">
                            <a class="nav-link " href="Facturi.php"><i class="far fa-circle nav-icon"></i><p>Facturi Emise</p></a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link " href="Incasari.php"><i class="far fa-circle nav-icon"></i><p>Incasari Lei</p></a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link " href="EditareIncasari.php"><i class="far fa-circle nav-icon"></i><p>Editare Incasari Lei</p></a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link " href="IncasariValuta.php"><i class="far fa-circle nav-icon"></i><p>Incasari Valuta</p></a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link " href="EditareIncasariValuta.php"><i class="far fa-circle nav-icon"></i><p>Editare Incasari Valuta</p></a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link " href="IncarcaIncasari.php"><i class="far fa-circle nav-icon"></i><p>Incarca Incasari LEI CSV</p></a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link " href="Viramente.php"><i class="far fa-circle nav-icon"></i><p>Export Viramente</p></a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link " href="ViramenteValuta.php"><i class="far fa-circle nav-icon"></i><p>Export Viramente Valuta</p></a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link " href="DeleteFacturi.php"><i class="far fa-circle nav-icon"></i><p>Sterge Facturi</p></a>
                        </li>
                    </ul>
                </li>

            </ul>
        </nav>
    </div></div></div><div class="os-scrollbar os-scrollbar-horizontal os-scrollbar-unusable"><div class="os-scrollbar-track"><div class="os-scrollbar-handle" style="width: 100%; transform: translate(0px, 0px);"></div></div></div><div class="os-scrollbar os-scrollbar-vertical"><div class="os-scrollbar-track"><div class="os-scrollbar-handle" style="height: 98.835%; transform: translate(0px, 0px);"></div></div></div><div class="os-scrollbar-corner"></div></div>
</aside>

  <div class="content-wrapper">
        <!-- Page Heading -->
        <header v-if="$slots.header">
                <slot name="header" />
        </header>
        <!-- Page Content -->
        <main>
            <slot />
        </main>
  </div>

    </div>
    <div>
        <Head :title="title" />

        <JetBanner />

        <div class="min-h-screen bg-gray-100">
            <nav class="bg-white border-b border-gray-100">
                <!-- Primary Navigation Menu -->
                <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                    <div class="flex justify-between h-16">
                        <div class="flex">
                            <!-- Logo -->
                            <div class="shrink-0 flex items-center">
                                <Link :href="route('dashboard')">
                                    <JetApplicationMark class="block h-9 w-auto" />
                                </Link>
                            </div>

                            <!-- Navigation Links -->
                            <div class="hidden space-x-8 sm:-my-px sm:ml-10 sm:flex">
                                <JetNavLink :href="route('dashboard')" :active="route().current('dashboard')">
                                    Dashboard
                                </JetNavLink>
                            </div>
                        </div>

                        <div class="hidden sm:flex sm:items-center sm:ml-6">
                            <div class="ml-3 relative">
                                <!-- Teams Dropdown -->
                                <JetDropdown v-if="$page.props.jetstream.hasTeamFeatures" align="right" width="60">
                                    <template #trigger>
                                        <span class="inline-flex rounded-md">
                                            <button type="button" class="inline-flex items-center px-3 py-2 border border-transparent text-sm leading-4 font-medium rounded-md text-gray-500 bg-white hover:bg-gray-50 hover:text-gray-700 focus:outline-none focus:bg-gray-50 active:bg-gray-50 transition">
                                                {{ $page.props.user.current_team.name }}

                                                <svg
                                                    class="ml-2 -mr-0.5 h-4 w-4"
                                                    xmlns="http://www.w3.org/2000/svg"
                                                    viewBox="0 0 20 20"
                                                    fill="currentColor"
                                                >
                                                    <path fill-rule="evenodd" d="M10 3a1 1 0 01.707.293l3 3a1 1 0 01-1.414 1.414L10 5.414 7.707 7.707a1 1 0 01-1.414-1.414l3-3A1 1 0 0110 3zm-3.707 9.293a1 1 0 011.414 0L10 14.586l2.293-2.293a1 1 0 011.414 1.414l-3 3a1 1 0 01-1.414 0l-3-3a1 1 0 010-1.414z" clip-rule="evenodd" />
                                                </svg>
                                            </button>
                                        </span>
                                    </template>

                                    <template #content>
                                        <div class="w-60">
                                            <!-- Team Management -->
                                            <template v-if="$page.props.jetstream.hasTeamFeatures">
                                                <div class="block px-4 py-2 text-xs text-gray-400">
                                                    Manage Team
                                                </div>

                                                <!-- Team Settings -->
                                                <JetDropdownLink :href="route('teams.show', $page.props.user.current_team)">
                                                    Team Settings
                                                </JetDropdownLink>

                                                <JetDropdownLink v-if="$page.props.jetstream.canCreateTeams" :href="route('teams.create')">
                                                    Create New Team
                                                </JetDropdownLink>

                                                <div class="border-t border-gray-100" />

                                                <!-- Team Switcher -->
                                                <div class="block px-4 py-2 text-xs text-gray-400">
                                                    Switch Teams
                                                </div>

                                                <template v-for="team in $page.props.user.all_teams" :key="team.id">
                                                    <form @submit.prevent="switchToTeam(team)">
                                                        <JetDropdownLink as="button">
                                                            <div class="flex items-center">
                                                                <svg
                                                                    v-if="team.id == $page.props.user.current_team_id"
                                                                    class="mr-2 h-5 w-5 text-green-400"
                                                                    fill="none"
                                                                    stroke-linecap="round"
                                                                    stroke-linejoin="round"
                                                                    stroke-width="2"
                                                                    stroke="currentColor"
                                                                    viewBox="0 0 24 24"
                                                                ><path d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" /></svg>
                                                                <div>{{ team.name }}</div>
                                                            </div>
                                                        </JetDropdownLink>
                                                    </form>
                                                </template>
                                            </template>
                                        </div>
                                    </template>
                                </JetDropdown>
                            </div>

                            <!-- Settings Dropdown -->
                            <div class="ml-3 relative">
                                <JetDropdown align="right" width="48">
                                    <template #trigger>
                                        <button v-if="$page.props.jetstream.managesProfilePhotos" class="flex text-sm border-2 border-transparent rounded-full focus:outline-none focus:border-gray-300 transition">
                                            <img class="h-8 w-8 rounded-full object-cover" :src="$page.props.user.profile_photo_url" :alt="$page.props.user.name">
                                        </button>

                                        <span v-else class="inline-flex rounded-md">
                                            <button type="button" class="inline-flex items-center px-3 py-2 border border-transparent text-sm leading-4 font-medium rounded-md text-gray-500 bg-white hover:text-gray-700 focus:outline-none transition">
                                                {{ $page.props.user.name }}

                                                <svg
                                                    class="ml-2 -mr-0.5 h-4 w-4"
                                                    xmlns="http://www.w3.org/2000/svg"
                                                    viewBox="0 0 20 20"
                                                    fill="currentColor"
                                                >
                                                    <path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd" />
                                                </svg>
                                            </button>
                                        </span>
                                    </template>

                                    <template #content>
                                        <!-- Account Management -->
                                        <div class="block px-4 py-2 text-xs text-gray-400">
                                            Manage Account
                                        </div>

                                        <JetDropdownLink :href="route('profile.show')">
                                            Profile
                                        </JetDropdownLink>

                                        <JetDropdownLink v-if="$page.props.jetstream.hasApiFeatures" :href="route('api-tokens.index')">
                                            API Tokens
                                        </JetDropdownLink>

                                        <div class="border-t border-gray-100" />

                                        <!-- Authentication -->
                                        <form @submit.prevent="logout">
                                            <JetDropdownLink as="button">
                                                Log Out
                                            </JetDropdownLink>
                                        </form>
                                    </template>
                                </JetDropdown>
                            </div>
                        </div>

                        <!-- Hamburger -->
                        <div class="-mr-2 flex items-center sm:hidden">
                            <button class="inline-flex items-center justify-center p-2 rounded-md text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:bg-gray-100 focus:text-gray-500 transition" @click="showingNavigationDropdown = ! showingNavigationDropdown">
                                <svg
                                    class="h-6 w-6"
                                    stroke="currentColor"
                                    fill="none"
                                    viewBox="0 0 24 24"
                                >
                                    <path
                                        :class="{'hidden': showingNavigationDropdown, 'inline-flex': ! showingNavigationDropdown }"
                                        stroke-linecap="round"
                                        stroke-linejoin="round"
                                        stroke-width="2"
                                        d="M4 6h16M4 12h16M4 18h16"
                                    />
                                    <path
                                        :class="{'hidden': ! showingNavigationDropdown, 'inline-flex': showingNavigationDropdown }"
                                        stroke-linecap="round"
                                        stroke-linejoin="round"
                                        stroke-width="2"
                                        d="M6 18L18 6M6 6l12 12"
                                    />
                                </svg>
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Responsive Navigation Menu -->
                <div :class="{'block': showingNavigationDropdown, 'hidden': ! showingNavigationDropdown}" class="sm:hidden">
                    <div class="pt-2 pb-3 space-y-1">
                        <JetResponsiveNavLink :href="route('dashboard')" :active="route().current('dashboard')">
                            Dashboard from applayout
                        </JetResponsiveNavLink>
                    </div>

                    <!-- Responsive Settings Options -->
                    <div class="pt-4 pb-1 border-t border-gray-200">
                        <div class="flex items-center px-4">
                            <div v-if="$page.props.jetstream.managesProfilePhotos" class="shrink-0 mr-3">
                                <img class="h-10 w-10 rounded-full object-cover" :src="$page.props.user.profile_photo_url" :alt="$page.props.user.name">
                            </div>

                            <div>
                                <div class="font-medium text-base text-gray-800">
                                    {{ $page.props.user.name }}
                                </div>
                                <div class="font-medium text-sm text-gray-500">
                                    {{ $page.props.user.email }}
                                </div>
                            </div>
                        </div>

                        <div class="mt-3 space-y-1">
                            <JetResponsiveNavLink :href="route('profile.show')" :active="route().current('profile.show')">
                                Profile
                            </JetResponsiveNavLink>

                            <JetResponsiveNavLink v-if="$page.props.jetstream.hasApiFeatures" :href="route('api-tokens.index')" :active="route().current('api-tokens.index')">
                                API Tokens
                            </JetResponsiveNavLink>

                            <!-- Authentication -->
                            <form method="POST" @submit.prevent="logout">
                                <JetResponsiveNavLink as="button">
                                    Log Out
                                </JetResponsiveNavLink>
                            </form>

                            <!-- Team Management -->
                            <template v-if="$page.props.jetstream.hasTeamFeatures">
                                <div class="border-t border-gray-200" />

                                <div class="block px-4 py-2 text-xs text-gray-400">
                                    Manage Team
                                </div>

                                <!-- Team Settings -->
                                <JetResponsiveNavLink :href="route('teams.show', $page.props.user.current_team)" :active="route().current('teams.show')">
                                    Team Settings
                                </JetResponsiveNavLink>

                                <JetResponsiveNavLink v-if="$page.props.jetstream.canCreateTeams" :href="route('teams.create')" :active="route().current('teams.create')">
                                    Create New Team
                                </JetResponsiveNavLink>

                                <div class="border-t border-gray-200" />

                                <!-- Team Switcher -->
                                <div class="block px-4 py-2 text-xs text-gray-400">
                                    Switch Teams
                                </div>

                                <template v-for="team in $page.props.user.all_teams" :key="team.id">
                                    <form @submit.prevent="switchToTeam(team)">
                                        <JetResponsiveNavLink as="button">
                                            <div class="flex items-center">
                                                <svg
                                                    v-if="team.id == $page.props.user.current_team_id"
                                                    class="mr-2 h-5 w-5 text-green-400"
                                                    fill="none"
                                                    stroke-linecap="round"
                                                    stroke-linejoin="round"
                                                    stroke-width="2"
                                                    stroke="currentColor"
                                                    viewBox="0 0 24 24"
                                                ><path d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" /></svg>
                                                <div>{{ team.name }}</div>
                                            </div>
                                        </JetResponsiveNavLink>
                                    </form>
                                </template>
                            </template>
                        </div>
                    </div>
                </div>
            </nav>

           
        </div>
    </div>
</template>
