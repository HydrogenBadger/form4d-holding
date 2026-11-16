# form4d.co.uk holding page

One page, "Website coming soon", until the full site (Documents\form4d-site) is ready. When it is, publish that folder to the same place instead.

## Putting it live (free: GitHub Pages + Namecheap DNS)

1. **GitHub:** create a public repository called `form4d-holding` (the free plan only serves Pages from public repositories), push this folder to branch `main`, then Settings > Pages > Deploy from a branch > `main` / root. Under Custom domain enter `form4d.co.uk`.
2. **Namecheap**, Domain List > form4d.co.uk > Manage > Advanced DNS: delete the parking records on `@` and `www`, then add

   | Type  | Host | Value                   |
   |-------|------|-------------------------|
   | A     | @    | 185.199.108.153         |
   | A     | @    | 185.199.109.153         |
   | A     | @    | 185.199.110.153         |
   | A     | @    | 185.199.111.153         |
   | CNAME | www  | hydrogenbadger.github.io |

3. **Email:** the page shows enquiries@form4d.co.uk. In Namecheap, form4d.co.uk > Manage > Redirect Email, add alias `enquiries` forwarding to your Gmail. Without this, mail to that address bounces. (`dave` forwards too, for invoices and direct contact.)
4. After DNS settles (minutes to a few hours), go back to GitHub Settings > Pages and tick **Enforce HTTPS**.

`form4d.uk` can point at the same page: Advanced DNS > URL Redirect Record, host `@`, value `https://form4d.co.uk`, permanent (301).
