Creating multiple applications within a single erlang node

- rebar.config in the root sub_dirs specifies (only). This tells rebar to pass commands issued at the root to all the apps (apps/*/) and the node (node/).

- the reltool.config in node/ points to "../apps" as it's lib_dir. This allows it to find the applications we place in the apps/ hierarchy.

- the reltool.config also contains mention of the desired apps in two places.

	- the rel section identifies the applications to "auto start"
	- the app section describes how the application is included into the node
	
	
