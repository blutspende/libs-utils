# utils
Various utility functions used throughout bloodlab.

###### Install
`go get github.com/blutspende/libs-utils`

## Slices
Contains utility functions for slices.
```go
func JoinByteSlicesWithLF(twoDim [][]byte) []byte
func JoinSingleLineByteSlicesWithLF(twoDim [][]byte) ([]byte, error)
func SplitByteSliceByLF(oneDim []byte) [][]byte
func JoinEnumsAsString[T ~string](enumList []T, separator string) string
func Partition(totalLength int, partitionLength int, consumer func(low int, high int) error) error
```

## Types
Contains type conversion utility functions. Converting between null, pointer, and normal representations of string, UUID, and time types.
```go
func StringToPointerWithNil(value string) *string
func StringPointerToString(value *string) string
func StringPointerToStringWithDefault(value *string, defaultValue string) string
func UUIDToNullUUID(value uuid.UUID) uuid.NullUUID
func NullUUIDToUUIDPointer(value uuid.NullUUID) *uuid.UUID
```