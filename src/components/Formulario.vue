<script setup>
    const props = defineProps(['valor1', 'valor2', 'alteraValor1', 'alteraValor2', 'operacao', 'alteraOperacao']);    
</script>

<template>
    <form>
        <div class="row">
            <div class="col">
                <input :value="props.valor1" @input="props.alteraValor1" type="number" class="form-control" inputmode="decimal" value="0" oninput="this.value = this.value.replace(/[^0-9.,]/g, '')" required placeholder="Insira o valor 1">
            </div>
            <div class="col">
                <input :value="props.valor2" @input="props.alteraValor2" type="number" class="form-control" inputmode="decimal" value="0" oninput="this.value = this.value.replace(/[^0-9.,]/g, '')" required placeholder="Insira o valor 2">
            </div>
            <div class="col-auto">
                <select :value="props.operacao" @change="props.alteraOperacao" class="form-control">
                    <option value="soma">Soma</option>
                    <option value="subtracao">Subtração</option>
                    <option value="multiplicacao">Multiplicação</option>
                    <option value="divisao">Divisão</option>
                </select>
            </div>
        </div>
    </form>
</template>