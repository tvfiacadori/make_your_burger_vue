<template>
    <div>
        <p>Component de Msg</p>
        <div>
            <form id="burger-form">
                <div class="input-container">
                    <label for="nome">Customer name:</label>
                    <input type="text" id="nome" name="nome" v-model="nome" placeholder="Put your name">
                </div>

                <div class="input-container">
                    <label for="pao">Choose the bread:</label>
                    <select name="pao" id="pao" v-model="pao">
                        <option value="">select your bread</option>
                        <option value="intregal">Integral</option>
                    </select>
                </div>

                <div class="input-container">
                    <label for="carne">Choose the meat:</label>
                    <select name="carne" id="carne" v-model="carne">
                        <option value="">select your meat</option>
                        <option value="chicken">Chicken</option>
                    </select>
                </div>

                <div id="options-container" class="input-container">
                    <label id="options-title" for="options">Choose the options:</label>
                   <div class="checkbox-container">
                        <input type="checkbox" name="options" v-model="options" value="salame">
                        <span>Salame</span>
                   </div>
                </div>

                <div class="input-container">
                    <input type="submit" class="submit-btn" value="Create my Burger !">
                </div>

            </form>
        </div>
    </div>
</template>

<script>
export default {
    name: "BurgerForm"
}
</script>

<style scoped>
    #burger-form {
        max-width: 400px;
        margin: 0 auto;
    }

    .input-container {
        display: flex;
        flex-direction: column;
        margin-bottom: 20px;    
    }

    label {
        font-weight: bold;
        margin-bottom: 15px;
        color: #222;
        padding: 5px 10px;
        border-left: 4px solid #fcba03;
    }

    input, select {
        padding: 5px 10px;
        width: 300px;
    }

    #options-container {
        flex-direction: row;
        flex-wrap: wrap;
    }

    #options-title {
        width: 100%;
    }

    #checkbox-container {
        display: flex;
        align-items: flex-start;
        width: 50%;
        margin-bottom: 20px;
    }

    .checkbox-container span,
    .checkbox-container input {
        width: auto;
    }

    .checkbox-container span {
        margin-left: 6px;
        font-weight: bold;
    }

    .submit-btn {
        background-color: #222;
        color: #fcba03;
        font-weight: bold;
        border: 2px solid #222;
        padding: 10px;
        font-size: 16px;
        margin: 0 auto;
        cursor: pointer;
        transition: .5s;
    }

    .submit-btn:hover {
        background-color: transparent;
        color: #222;
    }


</style>