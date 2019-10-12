<template>
    <div id="product">
        <h1>Product Create -Vue</h1>
        <p>
            <a :href="CreateProductUrl">Create New</a>
        </p>
        <table class="table">
            <thead>
                <tr>
                    <th>
                        Name
                    </th>
                    <th>
                        Price
                    </th>
                    <th></th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="item in Products">
                    <td>
                        {{item.Name}}
                    </td>
                    <td>
                        {{item.Price}}
                    </td>
                    <td>
                        <a :href="EditUrl+'/'+item.Id">Edit</a>|
                        <a :href="DetailsUrl+'/'+item.Id">Details</a> |
                        <a :href="DeleteUrl+'/'+item.Id">Delete</a>
                    </td>
                </tr>
            </tbody>
        </table>
    </div>
</template>
<script>
    export default {
        name: "product-create-component",
        props: {
            CreateProductUrl: String,
            DeleteUrl: String,
            EditUrl: String,
            DetailsUrl: String,
            Products: Array
        }
    };
</script>