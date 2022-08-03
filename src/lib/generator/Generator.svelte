<script>
    let headline = 'Certificate';
    let subheadline = 'of completion';
    let name = 'Dominik Schwind';
    let course = 'React for Beginners';
    let date = '03.08.2022';

    function createPdf() {
        let certificate = document.querySelector('.certificate');
        let options = {
            margin: 4,
            filename: `${name}.pdf`,
            jsPDF: { orientation: 'landscape' }
        }

		html2pdf().set(options).from(certificate).save();
	}
</script>

<div class="generator">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/html2pdf.js/0.9.3/html2pdf.bundle.min.js" integrity="sha512-YcsIPGdhPK4P/uRW6/sruonlYj+Q7UHWeKfTAkBW+g83NKM+jMJFJ4iAPfSnVp7BKD4dKMHmVSvICUbE/V1sSw==" crossorigin="anonymous" referrerpolicy="no-referrer"></script>
    <article class="certificate">
        <h2>{headline}</h2>
        <p>{subheadline}</p>
        <p>is awarded to</p>
        <p><b>{name}</b></p>
        <p>for completing</p>
        <p><i>{course}</i></p>

        <footer>
            <p>{date}</p>

            <div class="signature">
                <img src="signature.png">
            </div>
        </footer>

    </article>

    <form class="form">
        <div>
            <label for="headline">Headline</label>
            <input type="text" id="headline" name="headline" bind:value={headline}>
        </div>

        <div>
            <label for="headline">Subheadline</label>
            <input type="text" id="headline" name="headline" bind:value={subheadline}>
        </div>

        <div>
            <label for="headline">Name</label>
            <input type="text" id="headline" name="headline" bind:value={name}>
        </div>

        <div>
            <label for="headline">Course</label>
            <input type="text" id="headline" name="headline" bind:value={course}>
        </div>

        <div>
            <label for="headline">Date</label>
            <input type="text" id="headline" name="headline" bind:value={date}>
        </div>

        <button on:click={createPdf} type="button">
            PDF
        </button>
    </form>

</div>

<style>
    .generator {
        display: grid;
        grid-template-columns: 66% 33%;
        grid-gap: 1%;
    }

    .certificate {
        border: 1px solid black;
        aspect-ratio: 1.414 / 1;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        width: 90%;
    }

    label {
        font-weight: bold;
        width: 200px;
        display: inline-block;
    }

    footer {
        display: flex;
        margin-top: 10rem;
        justify-content: space-between;
        width: 90%;
    }
</style>
