include_directories(
  ${LLVM_MAIN_SRC_DIR}/lib/Target/LoongArch
  ${LLVM_BINARY_DIR}/lib/Target/LoongArch
  )

set(LLVM_LINK_COMPONENTS
  AsmParser
  CodeGen
  Core
  GlobalISel
  LoongArchCodeGen
  LoongArchDesc
  LoongArchInfo
  MC
  MIRParser
  SelectionDAG
  Support
  Target
  )

add_llvm_target_unittest(LoongArchTests
  InstSizes.cpp
  )

set_property(TARGET LoongArchTests PROPERTY FOLDER "Tests/UnitTests/TargetTests")
