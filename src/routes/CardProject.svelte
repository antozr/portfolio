<script>

export let titleCard
export let Subtitle
export let imgCard
export let cardWith
export let linkProject 

function viewProject(){
    window.open(linkProject);
}

</script>

<div class="card" style:background-image={`url("${imgCard}")`} style:width={cardWith} on:click={viewProject} aria-label="redirection vers le projet">
    <div class="card__box">
        <h3 class="sect__title--3 sect__title">
            {titleCard}
        </h3>
        <p class="sect__txt">
            {Subtitle}
        </p>
    </div>
</div>

<style lang="scss">

.card{
    background-position:top;
    background-repeat: no-repeat;
    background-size: cover;
    display: flex;
    flex-direction: row;
    align-items: flex-end;
   
    //border: 2px solid #000;
    aspect-ratio: 2/3;
    width: 100%;
    height: 280px;
    cursor: pointer;
    transition: .2s;

    &:hover{
        
        transition: 0.4s;
        border-radius: 30px  30px 0  ;
        transform: translateY(30px);
        

        &>div{
            border-bottom: 2px solid #FFBE5C;
            background-color: #FFBE5C;
            transition: 0.4s;
        }
    }

    
    
}
.card__box{
        width: 100%;
        height: auto;
        padding: 18px ;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: flex-end;
        background-color: #B9B1A6;
        row-gap: 12px;
        border-top: 2px solid #000;
        border-bottom: 2px solid #000;
        transition: 0.2s;

        
    }
.sect__title{
    text-align: end;
    width: 100%;
}
.sect__txt{
    text-align: end;
    width: 100%;
}

@media(min-width:600px){
    .card{

   
    //border: 2px solid #000;
    aspect-ratio: 2/3;
    width: calc(33% - 1vw);
    height: 480px;

    
}
}
</style>