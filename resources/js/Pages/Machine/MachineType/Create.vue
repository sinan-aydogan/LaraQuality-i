<template>
    <app-layout>
        <!--Header-->
        <template #header>
           Create New Machine Type
        </template>
        <!--Sub Header-->
        <template #sub-header>
            You can new machine type
        </template>
        <!--Action Buttons-->
        <template #action-buttons>
            <action-button label="Back to Machine Types List" :link="route('machine-type.index')" action="back"/>
        </template>
        <div class="relative w-full">
            <!--Content Table-->
            <form-content @submitted="save" @reset="reset">
                <form-section
                title="Machine Type Infos"
                description="You are going to create new machine type">
                    <!-- Name -->
                    <input-group label="Machine Type Name" labelFor="name" class="col-span-12">
                        <InputText id="name"  v-model="form.name"/>
                    </input-group>
                    <!-- Description -->
                    <input-group label="Descripton" labelFor="name" class="col-span-12">
                        <Textarea id="description" v-model="form.description" rows="3" cols="30" />
                    </input-group>
            </form-section>
            </form-content>
        </div>
    </app-layout>
</template>

<script>
import AppLayout from '@/Layouts/AppLayout'
import FormContent from '@/Components/Form/FormContent'
import FormSection from '@/Components/Form/FormSection'
import InputGroup from '@/Components/Form/InputGroup'
import Checked from '@/Components/Icons/General/Checked'
import XIcon from '@/Components/Icons/General/XIcon'
import ActionButton from '@/Components/Buttons/ActionButton'
/*PrimeVue Models*/
import InputText from 'primevue/inputtext'
import Dropdown from 'primevue/dropdown';
import SelectButton from 'primevue/selectbutton';
import Textarea from 'primevue/textarea';



export default {
    props: ['departments','standards'],
    components: {
        AppLayout,
        FormContent,
        FormSection,
        InputGroup,
        Checked,
        XIcon,
        InputText,
        Dropdown,
        SelectButton,
        ActionButton,
        Textarea
    },
    data() {
        return {
            form: this.$inertia.form({
                _method: 'POST',
                name : null,
                description : null,
            })
        };
    },
    methods: {
        reset: function () {
            this.form.name = null;
            this.form.description = null;
        },
        save() {
            this.form.post(route('machine-type.store'), {
                    errorBag: 'machine-type',
                    preserveScroll: true,
            });
            this.reset();
        },
    },
}
</script>
