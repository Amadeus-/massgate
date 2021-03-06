find_package(Zlib REQUIRED)

add_library(MCommon2
	ct_assert.h
	MC_Algorithm.h
	MC_Array.h
	MC_ArrayMap.h
	MC_BalancedITree.h
	MC_BalancedPTree.h
	MC_Base.h
	MC_BitVector.cpp
	MC_BitVector.h
	mc_circulararray.h
	MC_CircularGrowingArray.h
	mc_commandline.cpp
	mc_commandline.h
	MC_Constants.h
	MC_DataTypes.h
	MC_Debug.cpp
	MC_Debug.h
	MC_DebugListenerImplementations.cpp
	MC_DebugListenerImplementations.h
	MC_EggClockTimer.h
	MC_Endian.h
	mc_f2i.h
	MC_FastAlloc.cpp
	MC_FastAlloc.h
	mc_globaldefines.h
	MC_GrowingArray.h
	MC_HashMap.cpp
	MC_HashMap.h
	MC_HeapImplementation.h
	MC_HybridArray.h
	MC_IniFile.cpp
	MC_IniFile.h
	MC_Iterator.h
	MC_ITree.h
	MC_ITreeInorderIterator.h
	MC_ITreeLevelorderIterator.h
	MC_ITreeNode.h
	MC_ITreePostorderIterator.h
	MC_ITreePreorderIterator.h
	MC_KeyTree.h
	MC_KeyTreeInorderIterator.h
	MC_KeyTreeNode.h
	MC_KeyTreePostOrderIterator.h
	MC_Link.h
	MC_List.h
	MC_ListIterator.h
	MC_Math.h
	mc_md5.cpp
	mc_md5.h
	MC_Mem.cpp
	MC_Mem.h
	MC_MiniDumpTools.cpp
	MC_MiniDumpTools.h
	MC_Misc.cpp
	MC_Misc.h
	MC_Pair.h
	MC_Platform_Win32.cpp
	MC_Platform_Win32.h
	MC_Platform.h
	mc_prettyprinter.cpp
	mc_prettyprinter.h
	MC_Profiler.h
	MC_ProxyPtr.cpp
	MC_ProxyPtr.h
	MC_PTree.h
	MC_PTreeNode.h
	MC_Publisher.h
	MC_Registry.cpp
	MC_Registry.h
	MC_ScopedPtr.h
	MC_SmallObjectAllocator.h
	mc_sort.cpp
	mc_sort.h
	MC_SortedGrowingArray.h
	MC_Stack.h
	MC_StackList.h
	mc_stacktrace.cpp
	mc_stacktrace.h
	MC_StackWalker.cpp
	MC_StackWalker.h
	MC_StaticArray.h
	MC_String.cpp
	MC_String.h
	MC_StringParser.h
	MC_Subscriber.h
	MC_SystemPaths.cpp
	MC_SystemPaths.h
	MC_Tokenizer.h
	MC_Vector.h
	mf_file_platform.h
	mf_file_Win32.cpp
	mf_file.cpp
	mf_file.h
	mi_time.cpp
	mi_time.h
	mi_timechecker.cpp
	mi_timechecker.h
	mp_pack.cpp
	mp_pack.h
	MS_Aes.cpp
	MS_Aes.h
	MT_Event.cpp
	MT_Event.h
	MT_Job.cpp
	MT_Job.h
	MT_Mutex.cpp
	MT_Mutex.h
	MT_PooledThread.cpp
	MT_PooledThread.h
	MT_ReadWriteLock.cpp
	MT_ReadWriteLock.h
	MT_Semaphore.cpp
	MT_Semaphore.h
	MT_Supervisor.cpp
	MT_Supervisor.h
	MT_Task.cpp
	MT_Task.h
	MT_Thread.cpp
	MT_Thread.h
	MT_ThreadingTools.cpp
	MT_ThreadingTools.h
	MT_ThreadPool.cpp
	MT_ThreadPool.h
	MT_WorkerThread.cpp
	MT_WorkerThread.h
	StdAfx.cpp
	StdAfx.h
)

add_library(Lib::MCommon2 ALIAS MCommon2)

target_include_directories(MCommon2
	PUBLIC
		${CMAKE_CURRENT_SOURCE_DIR}
)

target_link_libraries(MCommon2
	PRIVATE
		dbghelp
	PUBLIC
		Zlib::Zlib
)

set_target_properties(MCommon2
	PROPERTIES
		CXX_STANDARD 98
		FOLDER "lib"
)