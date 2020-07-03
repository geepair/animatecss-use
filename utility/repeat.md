# 重复动画

> [!NOTE|label:注意]
>
> `V3.x`版本全部不适用

### repeat

| <p class="animated">repeat-1</p> | <p class="animated">repeat-2</p> |
| :------------------------------: | :------------------------------: |
| <p class="animated">repeat-3</p> | <p class="animated">infinite</p> |


<button id="callFunc">延迟重复动画</button>

> [!TIP|style:flat|label:Code]
>
> ~~<span class="tip">Old</span>（不适用）~~
>
> ```html
> <p class="animated bounce repeat-1">repeat-1</p>
> <p class="animated bounce repeat-2">repeat-2</p>
> <p class="animated bounce repeat-3">repeat-3</p>
> <p class="animated bounce infinite">infinite</p>
> ```
>
> <span class="tip">New</span>
> 
> ```html
> <p class="animate__animated animate__bounce animate__repeat-1">repeat-1</p>
> <p class="animate__animated animate__bounce animate__repeat-2">repeat-2</p>
> <p class="animate__animated animate__bounce animate__repeat-3">repeat-3</p>
> <p class="animate__animated animate__bounce infinite">infinite</p>
> ```

<script>
    document.getElementById('callFunc').addEventListener('click', ()=>{
        let anim = document.getElementsByClassName('animated')
        for(let i = 0; i < anim.length; i++) {
            anim[i].classList.add('bounce', anim[i].innerText)
            anim[i].addEventListener('animationend', ()=>{
                anim[i].classList.remove('bounce', anim[i].innerText)
            })
        }
    })
</script>