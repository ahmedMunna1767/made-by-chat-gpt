# DB Sequence Max-Length

The maximum length supported for a database sequence varies depending on the database management system (DBMS) being used.

In general, the maximum length for a sequence is limited by the maximum value that can be stored in the data type used by the sequence. For example, if the data type used by the sequence is an integer, the maximum length of the sequence will be limited by the maximum value that can be stored in that integer data type.

In Oracle, for example, the maximum value for a sequence is determined by the data type used by the sequence. If the sequence is created using the default data type of NUMBER, the maximum value is 28 digits. However, if the sequence is created using a larger data type, such as NUMBER(38), the maximum value can be much larger.

In PostgreSQL, the maximum value for a sequence is determined by the data type used by the sequence as well. The default data type for a sequence is integer, which has a maximum value of 2,147,483,647. However, larger data types, such as bigint or numeric, can be used to increase the maximum value.

In MySQL, the maximum value for a sequence is determined by the data type used by the sequence, with the default data type being bigint. The maximum value for a bigint data type is 9,223,372,036,854,775,807.

In summary, the maximum length supported for a database sequence varies depending on the DBMS being used and the data type used by the sequence. It is important to consult the documentation for the specific DBMS being used to determine the maximum length for a sequence.
