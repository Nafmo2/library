---
data:
  _extendedDependsOn: []
  _extendedRequiredBy: []
  _extendedVerifiedWith:
  - icon: ':x:'
    path: test/aoj/DSL_1_A.test.cpp
    title: test/aoj/DSL_1_A.test.cpp
  _isVerificationFailed: true
  _pathExtension: hpp
  _verificationStatusIcon: ':x:'
  attributes:
    links: []
  bundledCode: "#line 2 \"data_structure/unionfind.hpp\"\n\nstruct UnionFind {\n \
    \ vector< int > data;\n\n  UnionFind() = default;\n\n  explicit UnionFind(size_t\
    \ sz) : data(sz, -1) {}\n\n  bool unite(int x, int y) {\n    x = find(x), y =\
    \ find(y);\n    if(x == y) return false;\n    if(data[x] > data[y]) swap(x, y);\n\
    \    data[x] += data[y];\n    data[y] = x;\n    return true;\n  }\n\n  int find(int\
    \ k) {\n    if(data[k] < 0) return (k);\n    return data[k] = find(data[k]);\n\
    \  }\n\n  int size(int k) {\n    return -data[find(k)];\n  }\n\n  bool same(int\
    \ x, int y) {\n    return find(x) == find(y);\n  }\n\n  vector< vector< int >\
    \ > groups() {\n    int n = (int) data.size();\n    vector< vector< int > > ret(n);\n\
    \    for(int i = 0; i < n; i++) {\n      ret[find(i)].emplace_back(i);\n    }\n\
    \    ret.erase(remove_if(begin(ret), end(ret), [&](const vector< int > &v) {\n\
    \      return v.empty();\n    }), end(ret));\n    return ret;\n  }\n};\n"
  code: "#pragma once\n\nstruct UnionFind {\n  vector< int > data;\n\n  UnionFind()\
    \ = default;\n\n  explicit UnionFind(size_t sz) : data(sz, -1) {}\n\n  bool unite(int\
    \ x, int y) {\n    x = find(x), y = find(y);\n    if(x == y) return false;\n \
    \   if(data[x] > data[y]) swap(x, y);\n    data[x] += data[y];\n    data[y] =\
    \ x;\n    return true;\n  }\n\n  int find(int k) {\n    if(data[k] < 0) return\
    \ (k);\n    return data[k] = find(data[k]);\n  }\n\n  int size(int k) {\n    return\
    \ -data[find(k)];\n  }\n\n  bool same(int x, int y) {\n    return find(x) == find(y);\n\
    \  }\n\n  vector< vector< int > > groups() {\n    int n = (int) data.size();\n\
    \    vector< vector< int > > ret(n);\n    for(int i = 0; i < n; i++) {\n     \
    \ ret[find(i)].emplace_back(i);\n    }\n    ret.erase(remove_if(begin(ret), end(ret),\
    \ [&](const vector< int > &v) {\n      return v.empty();\n    }), end(ret));\n\
    \    return ret;\n  }\n};"
  dependsOn: []
  isVerificationFile: false
  path: data_structure/unionfind.hpp
  requiredBy: []
  timestamp: '2023-07-12 23:06:54+09:00'
  verificationStatus: LIBRARY_ALL_WA
  verifiedWith:
  - test/aoj/DSL_1_A.test.cpp
documentation_of: data_structure/unionfind.hpp
layout: document
redirect_from:
- /library/data_structure/unionfind.hpp
- /library/data_structure/unionfind.hpp.html
title: data_structure/unionfind.hpp
---