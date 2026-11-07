Reject Git revisions that begin with ``-`` when parsing ``git+`` URLs, so that a
crafted revision cannot be misinterpreted as a command-line option (argument
injection) by the underlying ``git checkout``/``reset``/``show-ref`` commands.
This mirrors the existing hardening of the Mercurial backend (CVE-2023-5752).
