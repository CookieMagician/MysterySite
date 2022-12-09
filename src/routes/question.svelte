<script>
    export let number;
    export let question;
    export let answer;
    export let check;
    let usrAnswer;

</script>

<div>
    <h3>Question {number}:</h3>
    <h3>{question}</h3>
    <input placeholder="Svar" bind:value={usrAnswer}>

    <button on:click={() => check(answer, usrAnswer)}>Check answer</button>
    <p class="error">That is not right!</p>
</div>

<style>
    .error {
        color: red;
    }
    img {
        position:absolute;
        width: 100%;
        height: 100%;
        top: 0px;
        left: 0px;
        pointer-events: none;
        opacity: 50%;
        z-index: -1;
    }
    h1 {
        color: greenyellow;
    }

    input {
        background-color: rgb(15, 15, 15);
        border-color: greenyellow;
        color: greenyellow;
    }
    button {
        background-color: rgb(15, 15, 15);
        color: greenyellow;
        border-color: greenyellow;
    }
</style>
