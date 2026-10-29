<template>
    <form>
        <div class="row">
            <div class="col">
                <input type="number" class="form-control" required placeholder="Insira o valor 1">
            </div>
            <div class="col">
                <input type="number" class="form-control" required placeholder="Insira o valor 2">
            </div>
            <div class="col-auto">
                <select class="form-control">
                    <option value="soma">Soma</option>
                    <option value="subtracao">Subtração</option>
                    <option value="multiplicacao">Multiplicação</option>
                    <option value="divisao">Divisão</option>
                </select>
            </div>
        </div>
    </form>
</template>