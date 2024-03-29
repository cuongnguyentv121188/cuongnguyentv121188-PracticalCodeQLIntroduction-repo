## 0.0.8

### New Queries

* The `security` tag has been added to the `cpp/return-stack-allocated-memory` query. As a result, its results will now appear by default.
* The "Uncontrolled data in arithmetic expression" (cpp/uncontrolled-arithmetic) query has been enhanced to reduce false positive results and its @precision increased to high.
* A new `cpp/very-likely-overruning-write` query has been added to the default query suite for C/C++. The query reports some results that were formerly flagged by `cpp/overruning-write`.

### Minor Analysis Improvements

* Fix an issue with the `cpp/declaration-hides-variable` query where it would report variables that are unnamed in a database.
* The `cpp/cleartext-storage-file` query has been upgraded with non-local taint flow and has been converted to a `path-problem` query.
* The `cpp/return-stack-allocated-memory` query has been improved to produce fewer false positives. The
  query has also been converted to a `path-problem` query.
* The "Cleartext transmission of sensitive information" (`cpp/cleartext-transmission`) query has been improved in several ways to reduce false positive results.
* The "Potential improper null termination" (`cpp/improper-null-termination`) query now produces fewer false positive results around control flow branches and loops.
* Added exception for GLib's gboolean to cpp/ambiguously-signed-bit-field.
  This change reduces the number of false positives in the query.

## 0.0.7

## 0.0.6

## 0.0.5

### New Queries

* A new query `cpp/certificate-not-checked` has been added for C/C++. The query flags unsafe use of OpenSSL and similar libraries.
* A new query `cpp/certificate-result-conflation` has been added for C/C++. The query flags unsafe use of OpenSSL and similar libraries.

## 0.0.4

### New Queries

* A new query `cpp/non-https-url` has been added for C/C++. The query flags uses of `http` URLs that might be better replaced with `https`.
