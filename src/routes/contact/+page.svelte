<script lang="ts">
    import Button from "$lib/components/ui/button/button.svelte";
    import Input from "$lib/components/ui/input/input.svelte";
    
    let currentInput: string = '';
    let previousInput: string = '';
    let operator: string = '';

    const appendNumber = (number: string | number) => {
        currentInput += number.toString();
    };

    const chooseOperation = (selectedOperator: string) => {
        if (currentInput === '') return;
        if (previousInput !== '') {
            compute();
        }
        operator = selectedOperator;
        previousInput = currentInput;
        currentInput = '';
    };

    const compute = () => {
        let computation: number | string;
        const prev = parseFloat(previousInput);
        const current = parseFloat(currentInput);

        if (isNaN(prev) || isNaN(current)) return;

        switch (operator) {
            case '+':
                computation = prev + current;
                break;
            case '-':
                computation = prev - current;
                break;
            case '*':
                computation = prev * current;
                break;
            case '/':
                computation = current === 0 ? 'Error' : prev / current;
                break;
            default:
                return;
        }
        currentInput = computation.toString();
        operator = '';
        previousInput = '';
    };

    const clear = () => {
        currentInput = '';
        previousInput = '';
        operator = '';
    };

    const deleteNumber = () => {
        currentInput = currentInput.slice(0, -1);
    };

    const updateDisplay = (): string => {
        return currentInput || previousInput || '0';
    };
</script>

<div class="flex flex-col w-full h-fit p-4 gap-4">
    <h1>Calculator</h1>
    <Input class="w-full" bind:value={currentInput}/>
    <div>{updateDisplay()}</div>
    <div class="grid grid-cols-4 gap-4">
        <Button on:click={clear}>AC</Button>
        <Button on:click={deleteNumber}>DEL</Button>
        <Button>Empty</Button>
        <Button on:click={() => chooseOperation('/')}>/</Button>
        <Button on:click={() => appendNumber(7)}>7</Button>
        <Button on:click={() => appendNumber(8)}>8</Button>
        <Button on:click={() => appendNumber(9)}>9</Button>
        <Button on:click={() => chooseOperation('*')}>*</Button>
        <Button on:click={() => appendNumber(4)}>4</Button>
        <Button on:click={() => appendNumber(5)}>5</Button>
        <Button on:click={() => appendNumber(6)}>6</Button>
        <Button on:click={() => chooseOperation('-')}>-</Button>
        <Button on:click={() => appendNumber(1)}>1</Button>
        <Button on:click={() => appendNumber(2)}>2</Button>
        <Button on:click={() => appendNumber(3)}>3</Button>
        <Button on:click={() => chooseOperation('+')}>+</Button>
        <Button on:click={() => appendNumber(0)}>0</Button>
        <Button on:click={() => appendNumber('.')}>.</Button>
        <Button on:click={compute} class="col-span-2">=</Button>
    </div>
</div>
