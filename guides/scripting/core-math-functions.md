# Core Math functions

### Table of Contents

1. Creating Vectors and Matrices
2. Accessing Vector Components
3. Vector and Matrix Operations
4. Binding Core Math Functions

### Creating Vectors and Matrices

#### Creating `vec2` objects

```lua
local v1 = vec2()
local v2 = vec2(1.0)
local v3 = vec2(1.0, 2.0)
```

#### Creating `vec3` objects

```lua
local v1 = glm.vec3()
local v2 = glm.vec3(1.0)
local v3 = glm.vec3(1.0, 2.0, 3.0)
```

#### Creating `vec4` objects

```lua
local v1 = glm.vec4()
local v2 = glm.vec4(1.0)
local v3 = glm.vec4(1.0, 2.0, 3.0, 4.0)
```

#### Creating `mat3` objects

```lua
local m1 = glm.mat3()
local m2 = glm.mat3(1.0)
local m3 = glm.mat3(glm.mat4())
local m4 = glm.mat3(1.0, 0.0, 0.0, 0.0, 1.0, 0.0, 0.0, 0.0, 1.0)
```

### Accessing Vector Components

#### Accessing `vec2` components

```lua
local x = vec2.x
local y = vec2.y
```

#### Accessing `vec3` components

```lua
local x = vec3.x
local y = vec3.y
local z = vec3.z
```

#### Accessing `vec4` components

```lua
local x = vec4.x
local y = vec4.y
local z = vec4.z
local w = vec4.w
```

### Vector and Matrix Operations

#### Addition

```lua
local result = vecA + vecB
local result = vecA + scalar
local result = scalar + vecA
```

#### Subtraction

```lua
local result = vecA - vecB
local result = vecA - scalar
local result = scalar - vecA
```

#### Multiplication

```lua
local result = vecA * vecB
local result = vecA * scalar
local result = scalar * vecA
local result = matA * vecA
```

#### Division

```lua
local result = vecA / vecB
local result = vecA / scalar
local result = scalar / vecA
```

#### Constants

```lua
local pi = glm.pi
local half_pi = glm.half_pi
local quarter_pi = glm.quarter_pi
local two_pi = glm.two_pi
```

#### Functions

```lua
local sqrt_result = glm.sqrt(x)
local pow_result = glm.pow(x, y)
local exp_result = glm.exp(x
```
