# MemoryDisposePOC.Net46
A performance and memory profiling project built with .NET Framework 4.6 to demonstrate the behavioral impact of using IDisposable properly. This proof-of-concept highlights how object disposal affects garbage collection (GC), memory usage, and runtime performance in older versions of the .NET Framework.
Output:
======== 🧪 OBJECT DISPOSAL TEST POC ======== 🔵 Test 1: With Proper Dispose ✅ Rows fetched: 5000 🔍 DataSet alive before GC? True 🔧 Manually triggering GC from: TestWithDispose() 🧪 Is DataSet Alive (after GC)? False ♻️ GC Count: Gen0 = 1, Gen1 = 0, Gen2 = 0 ⏱ Execution Time: 30 ms

------------------------------------------ 🔴 Test 2: Without Dispose ✅ Rows fetched: 5000 🔍 DataSet alive before GC? True ♻️ GC Count: Gen0 = 0, Gen1 = 0, Gen2 = 0 ⏱ Execution Time: 18 ms ======== ✅ TEST COMPLETE ========




# 🧪 DisposeEffectDotNet46 > A performance and memory profiling project using **.NET Framework 4.6** that compares application behavior when objects are **disposed properly** versus when they are **left undisposed**. The goal is to demonstrate how `IDisposable`, garbage collection (GC), and memory usage interact under different disposal patterns. --- ## 📌 Project Overview This proof-of-concept (POC) includes two test cases: 1. ✅ **With Dispose**: Objects are properly disposed using `using` blocks. 2. ❌ **Without Dispose**: Objects are not disposed, and strong references are retained. The project tracks: - 📈 Total memory usage (`GC.GetTotalMemory`) - ⏱ Execution time (`Stopwatch`) - ♻️ GC generation counts (`GC.CollectionCount`) - 🔍 Object lifetime via `WeakReference` --- ## 🏗️ Tech Stack | Component | Description | |----------------------|----------------------------| | Target Framework | .NET Framework 4.6 | | Language | C# | | IDE | Visual Studio 2015+ | | Runtime Tools Used | `System.Diagnostics`, `GC`, `WeakReference` | --- ## 📂 Folder Structure
