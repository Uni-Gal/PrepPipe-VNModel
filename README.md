
# TODO Documentation for PrepPipe's VNModel (Visual Novel IR)

[PrepPipe compiler](https://github.com/PrepPipe/preppipe-python) is a tool that compiles rich-text documents (.odt for now) into visual novel engine scripts (only RenPy for now). The compiler defines an Intermediate Representation (IR), VNModel, to describe an abstract (engine-agnostic) visual novel game. This repository contains the (WIP) documentation for VNModel.

PrepPipe compiler is built upon a base IR adapted from [MLIR project](https://mlir.llvm.org/). PrepPipe use this base IR to build higher-level IRs including VNModel.

The PrepPipe compiler is still experimental and we expect major changes in the IR definition during the development.

Note that the design purpose of VNModel is slightly different from existing UniGal's IR. PrepPipe compiler require the design of VNModel to support (1) code generation to multiple visual novel engine scripts (actually, PrepPipe tries to generate an entire game project or most part of it), and (2) compiler-based analysis and transform on the input game projects. The primary purpose does not include converting one VN script to another. Therefore, the information it contains is neither a subset nor the superset of what existing visual novel engine supports. However, once the PrepPipe compiler reaches maturity, if VNModel is equally capable of supporting translations of VN projects among different engines, we may try to make it part of the UniGal spec.
