Digitall-Demo Site as search site:

Precondition:
Deploy the customized module dx-base-demo-templates (from same git-source as the demo-site) and LDAP-provider from RQA5


The site is based on the digitall demo site, but has some extra content under section “Intranet”:


------------------------------------
CONTENT:
------------------------------------

Subsection INTRANET:
Only accessible for users (besides subpage Technology Trends)
PAGE Intranet
Paragraphs with visibility conditions
- Paragraph 1: not visible - visibility outdated
- Paragraph 2: visible (1 of 2 conditions matching)
- Paragraph 3: not visible - (all conditions should match - only 1 of 2)


PAGE Downloads
- column1: files for all users
- column2: images for all users
- column3: files & images only for group “Management”

PAGE Boards (blog-home)
- containing Blogs in live (UGC)

PAGE News
- Public news - content referenced from Newsroom/All News/Top Stories Area
- Internal news - 3 news entries, + referenced news from “Management News” (access limited to group Management)
- Management news - 4 news entries

PAGE Forum
- Forums - UGC (only in live)

PAGE Technology Trends (accessible for guest users)
- Paragraphs with categories
- comment block (UGC in live only)




------------------------------------
ROLES AND PERMISSIONS
------------------------------------

All over the site:
Edit roles
- Contributors: jane, user100, user110
- Editors: mathias, user0, user10
- Editors in chief: anne, user4, user14
- Reviewers: irina, user5, user15
- Site administrators: bill, user7, user17

Live roles:
- readers: Guest users, Users
- jahia-app user: users

Subpages under "Intranet"
- readers: Users (no guests allowed)


Intranet/Technology Trends
Live:
- readers: users, Guest user (also guests can access!)

Intranet/News/Internal News
Edit
- editors in chief: group Management
Live:
- readers: same as parent (Intranet)

Intranet/News/Management News
Edit:
- editors in chief: group Management
Live:
- readers: group Management



------------------------------------
USERS AND GROUPS:
------------------------------------

LDAP of RQA5 deployed

Groups:
- site administrators: bill, user7, user17
- Management:  user0, user1, anne, jay










