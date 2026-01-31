# RustAPI Benchmarks

This folder contains performance tests for the RustAPI framework.

## 🎯 Benchmark Types

### 1. Micro-benchmarks (Criterion.rs)
Tests the internal components of the framework:
- **Routing**: URL matching speed
- **JSON Serialization**: Serialize/deserialize performance
- **Extractors**: Path, Query, Json extractor speeds

### 2. HTTP Load Testing
End-to-end performance with real HTTP requests:
- **Hello World**: Simple text response
- **JSON Response**: JSON serialized response
- **Path Parameters**: Dynamic route parameters
- **JSON Parsing**: Request body parsing

## 🚀 Running Benchmarks

### Micro-benchmarks
```bash
cargo bench
```

### HTTP Load Tests (Automated Script)
```powershell
# Run the automated benchmark script
.\benches\run_benchmarks.ps1
```

## 📈 RustAPI vs Actix-web Comparison

| Feature | **RustAPI** | Actix-web | Axum | FastAPI (Python) |
|:-------|:-----------:|:---------:|:----:|:----------------:|
| **Performance** | **~92k req/s** | ~105k | ~100k | ~12k |
| **DX (Simplicity)** | 🟢 **High** | 🔴 Low | 🟡 Medium | 🟢 High |
| **Boilerplate** | **Zero** | High | Medium | Zero |
| **AI/LLM Native** | ✅ **Yes** | ❌ No | ❌ No | ❌ No |
| **Stability Logic** | 🛡️ **Facade** | ⚠️ Direct | ⚠️ Direct | ✅ Stable |


> Note: Benchmarks depend on system environment. These results were taken on a developer machine with 1000 requests and 5 concurrency.

## 🔥 Why RustAPI?

When compared to Actix-web, RustAPI offers:

### ✅ Advantages
1. **Developer Experience (DX)**: FastAPI-like ergonomics
2. **Automatic OpenAPI**: Documentation is automatically generated as you write code
3. **Built-in Validation**: Automatic 422 errors with `#[validate]` macros
4. **Simpler API**: Less boilerplate, more readable code
5. **Hyper 1.0**: Modern and stable HTTP stack

### 📊 Performance
- RustAPI delivers near Actix-web performance in raw speed (90-95%)
- This difference is negligible in real-world applications
- DX gains are more valuable than the small performance difference

### 🎯 When to Use RustAPI?
- API-first projects
- Projects requiring OpenAPI/Swagger documentation
- Rapid prototyping
- JSON-heavy REST APIs

### 🎯 When to Use Actix-web?
- Maximum raw performance is critical
- WebSocket-heavy applications
- Large projects requiring a mature ecosystem
