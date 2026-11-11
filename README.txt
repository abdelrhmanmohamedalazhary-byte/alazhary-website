ALAZHARY — Supabase-connected website

Contents
- index.html: complete website (HTML, CSS, and JavaScript in one file).

Supabase connection
- Uses the project's public anon key in the browser. This key is intended to be public; database security depends on Row Level Security policies.
- Reads only published rows from public.projects.
- Submits service requests to public.service_requests.
- Does not contain a service_role or sb_secret key.

Important checks before publishing
1. In Supabase, confirm RLS is enabled on projects and service_requests.
2. Confirm public.projects has a SELECT policy for anon that permits only status = 'published'.
3. Confirm public.service_requests has an INSERT policy for anon.
4. Submit a test request and confirm it appears in Table Editor > service_requests.
5. Never add a Supabase secret/service_role key to this file.

This is a static front end. It does not yet include the private admin dashboard, consultation form, contact-message form, or image storage workflow.
