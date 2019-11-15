<template>
  <div class="home">
    <b-card>
        <b-tabs card >
            <b-tab title="Alert" active><Alert/></b-tab>
            <b-tab title="Badge"><Badge/></b-tab>
            <b-tab title="Breadcrumb"><Breadcrumb/></b-tab>
            <b-tab title="Button Action"><ButtonAction/></b-tab> 
            <b-tab title="Card"><Card/></b-tab>     
            <b-tab title="Carousel"><Carousel/></b-tab>     
            <b-tab title="Collapse"><Collapse/></b-tab>                                    

            <b-tab title="Dropdown"><Dropdown/></b-tab>
            <b-tab title="Embed"><Embed/></b-tab>

            <b-tab title="Form"><Form/></b-tab>
            <b-tab title="Image"><Image/></b-tab>
            <b-tab title="Jumbotron"><Jumbotron/></b-tab> 
            <b-tab title="Modal"><Modal/></b-tab>
            
            <b-tab title="Navbar"><Navbar/></b-tab>
            <b-tab title="Pagination"><Pagination/></b-tab>

            <b-tab title="Table"><Table/></b-tab>
            <b-tab title="Tabs"><Tabs/></b-tab>
            <b-tab title="Toast"><Toast/></b-tab>

            <b-tab title="Utils"><Utils/></b-tab>  

        </b-tabs>
    </b-card>
</div>
</template>

<script>
// @ is an alias to /src
import Alert from '@/components/Alert.vue'

import Badge from '@/components/Badge.vue'
import Breadcrumb from '@/components/Breadcrumb.vue'
import ButtonAction from '@/components/ButtonAction.vue'


import Card from '@/components/Card.vue'
import Carousel from '@/components/Carousel.vue'
import Collapse from '@/components/Collapse.vue'

import Dropdown from '@/components/Dropdown.vue'
import Embed from '@/components/Embed.vue'

import Form from '@/components/Form.vue'
import Image from '@/components/Image.vue'
import Jumbotron from '@/components/Jumbotron.vue'
import Modal from '@/components/Modal.vue'


import Navbar from '@/components/Navbar.vue'
import Pagination from '@/components/Pagination.vue'
import Table from '@/components/Table.vue'
import Tabs from '@/components/Tabs.vue'
import Toast from '@/components/Toast.vue'

import Utils from '@/components/Utils.vue'


export default {
  name: 'home',
  components: {
    Alert,
    Badge,
    Breadcrumb,
    ButtonAction,
    Card,
    Carousel,
    Collapse,
    Dropdown,
    Embed,
    Form,
    Image,
    Jumbotron,
    Modal,
    Navbar,
    Pagination,
    Table,
    Tabs,
    Toast,
    Utils

  }
}
</script>
