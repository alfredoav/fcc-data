join_geo_sampling.sql is the query used in scripts/generate_maptiles.sh.
FRACTION must be replaced with a numeric fraction, which is done using sed.

concise_join_geo_sampling.sql fetches fewer fields but is otherwise the same
query as join_geo_sampling.sql.

join_geo.sql is the full version of join_geo_sampling; the latter has a filter to sample a fraction of the rows returned from the former, but the queries are otherwise the same.

join_state_geo.sql is an example query which joins the data for a single state,
given by STATENO. It is not currently designed for use in the scripts. If used
in the future, however, STATENO must too be replaced (just as FRACTION is), by a two-digit number representing a state (namely, its position in alphabetical order among states and territories).
