---
title: Ejemplo de modelo de eventos de ADO (VC ++)
TOCTitle: ADO Events Model example (VC++)
ms:assetid: 3785406b-844c-419f-e6ac-78aa8c4e78b2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249132(v=office.15)
ms:contentKeyID: 48544197
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1794e3e13bc2c8fe7c3acc9bbd1413daf4938d2c
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25859996"
---
# <a name="ado-events-model-example-vc"></a><span data-ttu-id="96489-102">Ejemplo de modelo de eventos de ADO (VC ++)</span><span class="sxs-lookup"><span data-stu-id="96489-102">ADO Events Model example (VC++)</span></span>


<span data-ttu-id="96489-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="96489-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="96489-104">En la sección [Creación de instancias de eventos de ADO por lenguaje](https://msdn.microsoft.com/library/jj250244\(v=office.15\)) de Visual C++, se ofrece una descripción general de cómo crear instancias del modelo de eventos de ADO.</span><span class="sxs-lookup"><span data-stu-id="96489-104">The Visual C++ section of [ADO Event Instantiation by Language](https://msdn.microsoft.com/library/jj250244\(v=office.15\)) gives a general description of how to instantiate the ADO event model.</span></span> <span data-ttu-id="96489-105">El siguiente es un ejemplo específico de creación de instancias del modelo de eventos dentro del entorno creado por la \*\* \#importar\*\* directiva.</span><span class="sxs-lookup"><span data-stu-id="96489-105">The following is a specific example of instantiating the event model within the environment created by the **\#import** directive.</span></span>

<span data-ttu-id="96489-106">La descripción general utiliza **adoint.h** como referencia para firmas de método.</span><span class="sxs-lookup"><span data-stu-id="96489-106">The general description uses **adoint.h** as a reference for method signatures.</span></span> <span data-ttu-id="96489-107">Sin embargo, algunos detalles de la descripción general cambian ligeramente debido al uso de la \*\* \#importar\*\* directiva:</span><span class="sxs-lookup"><span data-stu-id="96489-107">However, a few details in the general description change slightly as a result of using the **\#import** directive:</span></span>

  - <span data-ttu-id="96489-108">La \*\* \#importar\*\* directiva descompone los modificadores y tipos de datos de firma de método y **typedef**en sus formas fundamentales.</span><span class="sxs-lookup"><span data-stu-id="96489-108">The **\#import** directive resolves **typedef**'s, and method signature data types and modifiers to their fundamental forms.</span></span>

  - <span data-ttu-id="96489-109">Todos los métodos virtuales puros que se deben sobrescribir llevan el prefijo por "**sin procesar\_**".</span><span class="sxs-lookup"><span data-stu-id="96489-109">The pure virtual methods that must be overwritten are all prefixed by "**raw\_**".</span></span>

<span data-ttu-id="96489-110">Parte del código simplemente refleja el estilo de codificación.</span><span class="sxs-lookup"><span data-stu-id="96489-110">Some of the code simply reflects coding style.</span></span>

  - <span data-ttu-id="96489-111">El puntero a **IUnknown** utilizado por el método **Advise** se obtiene explícitamente con una llamada a **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="96489-111">The pointer to **IUnknown** used by the **Advise** method is obtained explicitly with a call to **QueryInterface**.</span></span>

  - <span data-ttu-id="96489-112">No es necesario codificar explícitamente un destructor en las definiciones de clase.</span><span class="sxs-lookup"><span data-stu-id="96489-112">You don't need to explicitly code a destructor in the class definitions.</span></span>

  - <span data-ttu-id="96489-113">Quizá desee codificar implementaciones más robustas de QueryInterface, AddRef y Release.</span><span class="sxs-lookup"><span data-stu-id="96489-113">You may want to code more robust implementations of QueryInterface, AddRef, and Release.</span></span>

  - <span data-ttu-id="96489-114">La \*\* \_ \_uuidof()\*\* directiva se utiliza ampliamente para obtener identificadores de interfaz.</span><span class="sxs-lookup"><span data-stu-id="96489-114">The **\_\_uuidof()** directive is used extensively to obtain interface IDs.</span></span>

<span data-ttu-id="96489-115">Por último, el ejemplo contiene parte de código funcional.</span><span class="sxs-lookup"><span data-stu-id="96489-115">Finally, the example contains some working code.</span></span>

  - <span data-ttu-id="96489-116">El ejemplo está escrito como una aplicación de consola.</span><span class="sxs-lookup"><span data-stu-id="96489-116">The example is written as a console application.</span></span>

  - <span data-ttu-id="96489-117">Deberá insertar su propio código bajo el comentario "/ / realizar algún trabajo".</span><span class="sxs-lookup"><span data-stu-id="96489-117">You should insert your own code under the comment, "// Do some work ".</span></span>

  - <span data-ttu-id="96489-p103">El comportamiento predeterminado de todos los controladores de eventos es no hacer nada y cancelar posteriores notificaciones. Por tanto, si se requiere, deberá insertar el código apropiado para su aplicación y permitir las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="96489-p103">All the event handlers default to doing nothing, and canceling further notifications. You should insert the appropriate code for your application, and allow notifications if required.</span></span>

<!-- end list -->

```cpp 
 
// eventmodel.cpp : Defines the entry point for the console application. 
// 
 
#import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
#include <comdef.h> 
#include <stdio.h> 
 
//----The Connection events---------------------------------------------- 
 
class CConnEvent : public ConnectionEventsVt 
{ 
private: 
 ULONG m_cRef; 
 public: 
 CConnEvent() { m_cRef = 0; }; 
 ~CConnEvent() {}; 
 
 
 STDMETHODIMP QueryInterface(REFIID riid, void ** ppv); 
 STDMETHODIMP_(ULONG) AddRef(void); 
 STDMETHODIMP_(ULONG) Release(void); 
 
 STDMETHODIMP raw_InfoMessage( 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Connection *pConnection); 
 
 STDMETHODIMP raw_BeginTransComplete( 
 LONG TransactionLevel, 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Connection *pConnection); 
 
 STDMETHODIMP raw_CommitTransComplete( 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Connection *pConnection); 
 
 STDMETHODIMP raw_RollbackTransComplete( 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Connection *pConnection); 
 
 STDMETHODIMP raw_WillExecute( 
 BSTR *Source, 
 CursorTypeEnum *CursorType, 
 LockTypeEnum *LockType, 
 long *Options, 
 EventStatusEnum *adStatus, 
 struct _Command *pCommand, 
 struct _Recordset *pRecordset, 
 struct _Connection *pConnection); 
 
 STDMETHODIMP raw_ExecuteComplete( 
 LONG RecordsAffected, 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Command *pCommand, 
 struct _Recordset *pRecordset, 
 struct _Connection *pConnection); 
 
 STDMETHODIMP raw_WillConnect( 
 BSTR *ConnectionString, 
 BSTR *UserID, 
 BSTR *Password, 
 long *Options, 
 EventStatusEnum *adStatus, 
 struct _Connection *pConnection); 
 
 STDMETHODIMP raw_ConnectComplete( 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Connection *pConnection); 
 
 STDMETHODIMP raw_Disconnect( 
 EventStatusEnum *adStatus, 
 struct _Connection *pConnection); 
}; 
 
//-----The Recordset events---------------------------------------------- 
 
class CRstEvent : public RecordsetEventsVt 
 { 
 private: 
 ULONG m_cRef; 
 public: 
 CRstEvent() { m_cRef = 0; }; 
 ~CRstEvent() {}; 
 
 STDMETHODIMP QueryInterface(REFIID riid, void ** ppv); 
 STDMETHODIMP_(ULONG) AddRef(void); 
 STDMETHODIMP_(ULONG) Release(void); 
 
 STDMETHODIMP raw_WillChangeField( 
 LONG cFields, 
 VARIANT Fields, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset); 
 
 STDMETHODIMP raw_FieldChangeComplete( 
 LONG cFields, 
 VARIANT Fields, 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset); 
 
 STDMETHODIMP raw_WillChangeRecord( 
 EventReasonEnum adReason, 
 LONG cRecords, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset); 
 
 STDMETHODIMP raw_RecordChangeComplete( 
 EventReasonEnum adReason, 
 LONG cRecords, 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset); 
 
 STDMETHODIMP raw_WillChangeRecordset( 
 EventReasonEnum adReason, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset); 
 
 STDMETHODIMP raw_RecordsetChangeComplete( 
 EventReasonEnum adReason, 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset); 
 
 STDMETHODIMP raw_WillMove( 
 EventReasonEnum adReason, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset); 
 
 STDMETHODIMP raw_MoveComplete( 
 EventReasonEnum adReason, 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset); 
 
 STDMETHODIMP raw_EndOfRecordset( 
 VARIANT_BOOL *fMoreData, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset); 
 
 STDMETHODIMP raw_FetchProgress( 
 long Progress, 
 long MaxProgress, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset); 
 
 STDMETHODIMP raw_FetchComplete( 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset); 
}; 
 
 
//-----Implement each connection method---------------------------------- 
 
 STDMETHODIMP CConnEvent::raw_InfoMessage( 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Connection *pConnection) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CConnEvent::raw_BeginTransComplete( 
 LONG TransactionLevel, 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Connection *pConnection) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CConnEvent::raw_CommitTransComplete( 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Connection *pConnection) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CConnEvent::raw_RollbackTransComplete( 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Connection *pConnection) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CConnEvent::raw_WillExecute( 
 BSTR *Source, 
 CursorTypeEnum *CursorType, 
 LockTypeEnum *LockType, 
 long *Options, 
 EventStatusEnum *adStatus, 
 struct _Command *pCommand, 
 struct _Recordset *pRecordset, 
 struct _Connection *pConnection) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CConnEvent::raw_ExecuteComplete( 
 LONG RecordsAffected, 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Command *pCommand, 
 struct _Recordset *pRecordset, 
 struct _Connection *pConnection) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CConnEvent::raw_WillConnect( 
 BSTR *ConnectionString, 
 BSTR *UserID, 
 BSTR *Password, 
 long *Options, 
 EventStatusEnum *adStatus, 
 struct _Connection *pConnection) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CConnEvent::raw_ConnectComplete( 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Connection *pConnection) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CConnEvent::raw_Disconnect( 
 EventStatusEnum *adStatus, 
 struct _Connection *pConnection) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 
//-----Implement each recordset method----------------------------------- 
 
 STDMETHODIMP CRstEvent::raw_WillChangeField( 
 LONG cFields, 
 VARIANT Fields, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CRstEvent::raw_FieldChangeComplete( 
 LONG cFields, 
 VARIANT Fields, 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CRstEvent::raw_WillChangeRecord( 
 EventReasonEnum adReason, 
 LONG cRecords, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CRstEvent::raw_RecordChangeComplete( 
 EventReasonEnum adReason, 
 LONG cRecords, 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CRstEvent::raw_WillChangeRecordset( 
 EventReasonEnum adReason, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CRstEvent::raw_RecordsetChangeComplete( 
 EventReasonEnum adReason, 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CRstEvent::raw_WillMove( 
 EventReasonEnum adReason, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CRstEvent::raw_MoveComplete( 
 EventReasonEnum adReason, 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CRstEvent::raw_EndOfRecordset( 
 VARIANT_BOOL *fMoreData, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CRstEvent::raw_FetchProgress( 
 long Progress, 
 long MaxProgress, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 STDMETHODIMP CRstEvent::raw_FetchComplete( 
 struct Error *pError, 
 EventStatusEnum *adStatus, 
 struct _Recordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 }; 
 
 
//-----Implement QueryInterface, AddRef, and Release--------------------- 
 
 STDMETHODIMP CRstEvent::QueryInterface(REFIID riid, void ** ppv) 
 { 
 *ppv = NULL; 
 if (riid == __uuidof(IUnknown) || 
 riid == __uuidof(RecordsetEventsVt)) *ppv = this; 
 if (*ppv == NULL) 
 return ResultFromScode(E_NOINTERFACE); 
 AddRef(); 
 return NOERROR; 
 } 
 STDMETHODIMP_(ULONG) CRstEvent::AddRef(void) { return ++m_cRef; }; 
 STDMETHODIMP_(ULONG) CRstEvent::Release() 
 { 
 if (0 != --m_cRef) return m_cRef; 
 delete this; 
 return 0; 
 } 
 
 STDMETHODIMP CConnEvent::QueryInterface(REFIID riid, void ** ppv) 
 
 { 
 *ppv = NULL; 
 if (riid == __uuidof(IUnknown) || 
 riid == __uuidof(ConnectionEventsVt)) *ppv = this; 
 if (*ppv == NULL) 
 return ResultFromScode(E_NOINTERFACE); 
 AddRef(); 
 return NOERROR; 
 } 
 STDMETHODIMP_(ULONG) CConnEvent::AddRef() { return ++m_cRef; }; 
 STDMETHODIMP_(ULONG) CConnEvent::Release() 
 { 
 if (0 != --m_cRef) return m_cRef; 
 delete this; 
 return 0; 
 } 
 
//-----Write your main block of code------------------------------------- 
 
int main(int argc, char* argv[]) 
{ 
 HRESULT hr; 
 DWORD dwConnEvt; 
 DWORD dwRstEvt; 
 IConnectionPointContainer *pCPC = NULL; 
 IConnectionPoint *pCP = NULL; 
 IUnknown *pUnk = NULL; 
 CRstEvent *pRstEvent = NULL; 
 CConnEvent *pConnEvent= NULL; 
 int rc = 0; 
 _RecordsetPtr pRst; 
 _ConnectionPtr pConn; 
 
 ::CoInitialize(NULL); 
 
 hr = pConn.CreateInstance(__uuidof(Connection)); 
 if (FAILED(hr)) return rc; 
 
 hr = pRst.CreateInstance(__uuidof(Recordset)); 
 if (FAILED(hr)) return rc; 
 
 // Start using the Connection events 
 
 hr = pConn->QueryInterface(__uuidof(IConnectionPointContainer), 
 (void **)&pCPC); 
 if (FAILED(hr)) return rc; 
 hr = pCPC->FindConnectionPoint(__uuidof(ConnectionEvents), &pCP); 
 pCPC->Release(); 
 if (FAILED(hr)) return rc; 
 
 pConnEvent = new CConnEvent(); 
 hr = pConnEvent->QueryInterface(__uuidof(IUnknown), (void **) &pUnk); 
 if (FAILED(hr)) return rc; 
 hr = pCP->Advise(pUnk, &dwConnEvt); 
 pCP->Release(); 
 if (FAILED(hr)) return rc; 
 
 // Start using the Recordset events 
 
 hr = pRst->QueryInterface(__uuidof(IConnectionPointContainer), 
 (void **)&pCPC); 
 if (FAILED(hr)) return rc; 
 hr = pCPC->FindConnectionPoint(__uuidof(RecordsetEvents), &pCP); 
 pCPC->Release(); 
 if (FAILED(hr)) return rc; 
 
 pRstEvent = new CRstEvent(); 
 hr = pRstEvent->QueryInterface(__uuidof(IUnknown), (void **) &pUnk); 
 if (FAILED(hr)) return rc; 
 hr = pCP->Advise(pUnk, &dwRstEvt); 
 pCP->Release(); 
 if (FAILED(hr)) return rc; 
 
 // Do some work 
 
 pConn->Open("dsn=Pubs;", "MyUserName", "MyPassword", adConnectUnspecified); 
 pRst->Open("SELECT * FROM authors", (IDispatch *) pConn, 
 adOpenStatic, adLockReadOnly, adCmdText); 
 pRst->MoveFirst(); 
 while (pRst->EndOfFile == FALSE) 
 { 
 wprintf(L"Name = '%s'\n", (wchar_t*) 
 ((_bstr_t) pRst->Fields->GetItem("au_lname")->Value)); 
 pRst->MoveNext(); 
 } 
 
 pRst->Close(); 
 pConn->Close(); 
 
 // Stop using the Connection events 
 
 hr = pConn->QueryInterface(__uuidof(IConnectionPointContainer), 
 (void **) &pCPC); 
 if (FAILED(hr)) return rc; 
 hr = pCPC->FindConnectionPoint(__uuidof(ConnectionEvents), &pCP); 
 pCPC->Release(); 
 if (FAILED(hr)) return rc; 
 hr = pCP->Unadvise( dwConnEvt ); 
 pCP->Release(); 
 if (FAILED(hr)) return rc; 
 
 // Stop using the Recordset events 
 hr = pRst->QueryInterface(__uuidof(IConnectionPointContainer), 
 (void **) &pCPC); 
 if (FAILED(hr)) return rc; 
 hr = pCPC->FindConnectionPoint(__uuidof(RecordsetEvents), &pCP); 
 pCPC->Release(); 
 if (FAILED(hr)) return rc; 
 hr = pCP->Unadvise( dwRstEvt ); 
 pCP->Release(); 
 if (FAILED(hr)) return rc; 
 
 CoUninitialize(); 
 return 1; 
} 
```

