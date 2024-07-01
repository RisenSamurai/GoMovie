<script>

    import Button from "$lib/components/Button.svelte";

    let message = "";
    let director = "";
    let writer = "";
    let producer = "";
    let editor = "";
    let camera = "";
    let genre = "";
    let country = "";

    let directors = [];
    let writers = [];
    let producers = [];
    let editors = [];
    let cameras = [];
    let genres = [];
    let countries = [];
    let images = [];
    let actors = [];



    function pushDirector(person, type) {

        switch (type) {
            case "d": {
                directors = [...directors, person];
                director = "";
            } break;
            case "w": {
                writers = [...writers, person];
                writer = "";
            } break;
            case "p": {
                producers = [...producers, person];
                producer = "";
            } break;
            case "e": {
                editors = [...editors, person];
                editor = "";
            } break;
            case "c": {
                cameras = [...cameras, person];
                camera = "";
            } break;
            case "g": {
                genres = [...genres, person];
                genre = "";
            }
        }


    }

    function removeDirector(index, type) {

        switch (type) {
            case "d": {
                directors = directors.filter((_, i) => i !== index);
            } break;

            case "w": {
                writers = writers.filter((_, i) => i !== index);
            } break;

            case "p": {
                producers = producers.filter((_, i) => i !== index);
            } break;

            case "e": {
                editors = editors.filter((_, i) => i !== index);
            } break;

            case "c": {
                cameras = cameras.filter((_, i) => i !== index);
            } break;

            case "g": {
                genres = genres.filter((_, i) => i !== index);
            }
        }


    }


</script>



<h2 class="text-2xl text-white">{#if message}{message}{/if}</h2>
<form on:submit class="flex flex-col bg-cinema-secondary w-full">
    <fieldset class="flex flex-col p-2">
        <legend class="flex font-bold text-cinema-text text-xl">Basic Info</legend>
        <label class="text-cinema-text" for="movie-name">Movie Name</label>
        <input class="p-1 rounded-lg mb-2" type="text" name="movie-name" id="movie-name">
        <label class="text-cinema-text" for="year">Year</label>
        <input class="p-1 rounded-lg mb-2" type="text" name="lastName" id="year">
    </fieldset>

    <fieldset class="flex flex-col p-2">
        <legend class="flex font-bold text-cinema-text text-xl">Film Crew</legend>
        <label class="text-cinema-text" for="director">Director</label>
        <input bind:value={director} class="p-1 rounded-lg mb-2" type="text" name="director" id="director">

        {#if directors.length > 0}
            <div class="flex flex-wrap">

                {#each directors as director, index}
                    <div class="flex justify-between items-center pl-2">
                        <span class="text-cinema-text">{director}</span>
                        <button type="button" class="text-cinema-text font-bold text-xl ml-2"
                                on:click={() => removeDirector(index, "d")}>X</button>
                    </div>
                    {/each}

            </div>
        {/if}
        <Button padding="p-2" name="Push" on:click={() => pushDirector(director, "d")} />

        <label class="text-cinema-text" for="director">Writers</label>
        <input bind:value={writer} class="p-1 rounded-lg mb-2" type="text" name="director" id="director">

        {#if directors.length > 0}
            <div class="flex flex-wrap">

                {#each writers as writer, index}
                    <div class="flex justify-between items-center pl-2">
                        <span class="text-cinema-text">{writer}</span>
                        <button type="button" class="text-cinema-text font-bold text-xl ml-2"
                                on:click={() => removeDirector(index, "w")}>X</button>
                    </div>
                {/each}

            </div>
        {/if}
        <Button padding="p-2" name="Push" on:click={() => pushDirector(writer, "w")} />


        <label class="text-cinema-text" for="director">Producers</label>
        <input bind:value={writer} class="p-1 rounded-lg mb-2" type="text" name="director" id="director">

        {#if producers.length > 0}
            <div class="flex flex-wrap">

                {#each producers as writer, index}
                    <div class="flex justify-between items-center pl-2">
                        <span class="text-cinema-text">{writer}</span>
                        <button type="button" class="text-cinema-text font-bold text-xl ml-2"
                                on:click={() => removeDirector(index, "p")}>X</button>
                    </div>
                {/each}

            </div>
        {/if}
        <Button padding="p-2" name="Push" on:click={() => pushDirector(producer, "p")} />

        <label class="text-cinema-text" for="director">Editors</label>
        <input bind:value={writer} class="p-1 rounded-lg mb-2" type="text" name="director" id="director">

        {#if editors.length > 0}
            <div class="flex flex-wrap">

                {#each editors as editor, index}
                    <div class="flex justify-between items-center pl-2">
                        <span class="text-cinema-text">{editor}</span>
                        <button type="button" class="text-cinema-text font-bold text-xl ml-2"
                                on:click={() => removeDirector(index, "e")}>X</button>
                    </div>
                {/each}

            </div>
        {/if}
        <Button padding="p-2" name="Push" on:click={() => pushDirector(editor, "e")} />

        <label class="text-cinema-text" for="director">Cameras</label>
        <input bind:value={writer} class="p-1 rounded-lg mb-2" type="text" name="director" id="director">

        {#if cameras.length > 0}
            <div class="flex flex-wrap">

                {#each cameras as camera, index}
                    <div class="flex justify-between items-center pl-2">
                        <span class="text-cinema-text">{camera}</span>
                        <button type="button" class="text-cinema-text font-bold text-xl ml-2"
                                on:click={() => removeDirector(index, "c")}>X</button>
                    </div>
                {/each}

            </div>
        {/if}
        <Button padding="p-2" name="Push" on:click={() => pushDirector(camera, "c")} />

        <label class="text-cinema-text" for="director">Genres</label>
        <input bind:value={writer} class="p-1 rounded-lg mb-2" type="text" name="director" id="director">

        {#if genres.length > 0}
            <div class="flex flex-wrap">

                {#each genres as genre, index}
                    <div class="flex justify-between items-center pl-2">
                        <span class="text-cinema-text">{genre}</span>
                        <button type="button" class="text-cinema-text font-bold text-xl ml-2"
                                on:click={() => removeDirector(index, "g")}>X</button>
                    </div>
                {/each}

            </div>
        {/if}
        <Button padding="p-2" name="Push" on:click={() => pushDirector(genre, "g")} />

    </fieldset>

    <fieldset class="flex flex-col p-2">
        <legend class="flex font-bold text-cinema-text text-xl">Release date</legend>
        <input type="date" name="date">
    </fieldset>

    <fieldset class="flex flex-col p-2">
        <legend class="flex font-bold text-cinema-text text-xl">Other</legend>
        <label class="text-cinema-text" for="country">Countries</label>
        <input bind:value={writer} class="p-1 rounded-lg mb-2" type="text" name="country" id="country">

        {#if countries.length > 0}
            <div class="flex flex-wrap">

                {#each countries as country, index}
                    <div class="flex justify-between items-center pl-2">
                        <span class="text-cinema-text">{country}</span>
                        <button type="button" class="text-cinema-text font-bold text-xl ml-2"
                                on:click={() => removeDirector(index, "country")}>X</button>
                    </div>
                {/each}

            </div>
        {/if}
        <Button padding="p-2" name="Push" on:click={() => pushDirector(country, "country")} />


        <label class="text-cinema-text" for="duration">Duration(min)</label>
        <input class="p-1 rounded-lg mb-2" type="text" name="duration" id="duration">

        <label class="text-cinema-text" for="description">Description</label>
        <textarea class="p-1 rounded-lg mb-2" name="description" id="description" cols="10" rows="5"></textarea>

    </fieldset>

</form>