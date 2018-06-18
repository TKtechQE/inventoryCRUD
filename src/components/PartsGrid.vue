<template>
    <div class="partsgrid">
        <c-grid class="partsgrid" ref="grid" :data="records" :frozen-col-count="1">
            <c-grid-column :width="50" field="check" column-type="check" action="check" />
            <c-grid-column field="personid" width="85">
                ID
            </c-grid-column>
            <c-grid-column-group caption="Name">
                <c-grid-input-column field="fname" width="20%" min-width="150">
                    First Name
                </c-grid-input-column>
                <c-grid-input-column field="lname" width="20%" min-width="150">
                    Last Name
                </c-grid-input-column>
            </c-grid-column-group>
            <c-grid-button-column caption="SHOW REC" width="120" @click="onClickRecord"/>
        </c-grid>
    </div>
</template>

<script>
    export default {
        name: 'PartsGrid',
        props: {},
        data: function () {
            return {
                records: [
                            {'personid': 1, 'fname': 'Sophia', 'lname': 'Hill', 'email': 'sophia_hill@example.com'},
                            {'personid': 2, 'fname': 'Aubrey', 'lname': 'Martin', 'email': 'aubrey_martin@example.com'},
                            {'personid': 3, 'fname': 'Avery', 'lname': 'Jones', 'email': 'avery_jones@example.com'},
                            {'personid': 4, 'fname': 'Joseph', 'lname': 'Rodriguez', 'email': 'joseph_rodriguez@example.com'},
                            {'personid': 5, 'fname': 'Samuel', 'lname': 'Campbell', 'email': 'samuel_campbell@example.com'},
                            {'personid': 6, 'fname': 'Joshua', 'lname': 'Ortiz', 'email': 'joshua_ortiz@example.com'},
                            {'personid': 7, 'fname': 'Mia', 'lname': 'Foster', 'email': 'mia_foster@example.com'},
                            {'personid': 8, 'fname': 'Landon', 'lname': 'Lopez', 'email': 'landon_lopez@example.com'},
                            {'personid': 9, 'fname': 'Audrey', 'lname': 'Cox', 'email': 'audrey_cox@example.com'},
                            {'personid': 10, 'fname': 'Anna', 'lname': 'Ramirez', 'email': 'anna_ramirez@example.com'}
                ]
            }
        },
        methods: {
            onClickRecord(rec) {
                alert(JSON.stringify(rec))
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>