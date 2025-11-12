<script lang="ts">
    const contacts = [
        { title: "Email",    link: "mailto:jakobsereda@gmail.com",            body: "jakobsereda@gmail.com"       },
        { title: "GitHub",   link: "https://www.github.com/jakobsereda",      body: "github.com/jakobsereda"      },
        { title: "LinkedIn", link: "https://www.linkedin.com/in/jakobsereda", body: "linkedin.com/in/jakobsereda" },
    ];
</script>

<div class="flex flex-col gap-4">
    <p>
        Want to get in touch? You can reach me via:
    </p>
    <ul class="list-disc list-inside ml-4">
    {#each contacts as contact}
        <li>
            {contact.title}: 
            <a href="{contact.link}" target="_blank" class="text-gruvbox-blue0 dark:text-gruvbox-green1">
                {contact.body}
            </a>
        </li>
    {/each}
    </ul>
</div>

<style>
	a {
		transition: transform 0.2s ease;
	}

	a:hover {
		text-decoration: underline;
	}
</style>
