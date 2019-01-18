---
title: Visual C++ (referencia de escritorio de la base de datos de Access)
TOCTitle: Visual C++
ms:assetid: 31d27968-e7bd-02fa-efad-26039bea30b8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249091(v=office.15)
ms:contentKeyID: 48544062
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 082790c33840bfeacf0c1a6bd38af34c0617f4fe
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718773"
---
# <a name="visual-c"></a><span data-ttu-id="2c04c-102">Visual C++</span><span class="sxs-lookup"><span data-stu-id="2c04c-102">Visual C++</span></span>


<span data-ttu-id="2c04c-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2c04c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2c04c-104">Esta es una descripción esquemática de cómo crear instancias de eventos de ADO en Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="2c04c-104">This is a schematic description of how to instantiate ADO events in Microsoft Visual C++.</span></span> <span data-ttu-id="2c04c-105">Vea [ejemplo de modelo de eventos de ADO (VC ++)](ado-events-model-example-vc.md) para obtener una descripción completa.</span><span class="sxs-lookup"><span data-stu-id="2c04c-105">See [ADO Events Model example (VC++)](ado-events-model-example-vc.md) for a complete description.</span></span>

<span data-ttu-id="2c04c-106">Cree clases derivadas de las interfaces **ConnectionEventsVt** y **RecordsetEventsVt** incluidas en el archivo adoint.h.</span><span class="sxs-lookup"><span data-stu-id="2c04c-106">Create classes derived from the **ConnectionEventsVt** and **RecordsetEventsVt** interfaces found in the file adoint.h.</span></span>

```cpp 
 
// BeginEventExampleVC01 
class CConnEvent : public ConnectionEventsVt 
{ 
 public: 
 STDMETHODIMP InfoMessage( 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADOConnection *pConnection); 
... 
} 
 
class CRstEvent : public RecordsetEventsVt 
{ 
 public: 
 STDMETHODIMP WillChangeField( 
 LONG cFields, 
 VARIANT Fields, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset); 
... 
} 
// EndEventExampleVC01 
```

<span data-ttu-id="2c04c-107">Implemente cada uno de los métodos event-handler en ambas clases.</span><span class="sxs-lookup"><span data-stu-id="2c04c-107">Implement each of the event-handler methods in both classes.</span></span> <span data-ttu-id="2c04c-108">Basta con que cada método devuelva un HRESULT de S\_Aceptar.</span><span class="sxs-lookup"><span data-stu-id="2c04c-108">It is sufficient that each method merely return an HRESULT of S\_OK.</span></span> <span data-ttu-id="2c04c-109">Sin embargo, cuando notifique que los controladores de eventos están disponibles, se les llamará continuamente de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2c04c-109">However, when you make it known that your event handlers are available, they will be called continuously by default.</span></span> <span data-ttu-id="2c04c-110">En lugar de ello, tal vez desee que no se soliciten más notificaciones después de la primera vez estableciendo **adStatus** en **adStatusUnwantedEvent**.</span><span class="sxs-lookup"><span data-stu-id="2c04c-110">Instead, you might want to request no further notification after the first time by setting **adStatus** to **adStatusUnwantedEvent**.</span></span>

```cpp 
 
// BeginEventExampleVC02 
STDMETHODIMP CConnEvent::ConnectComplete( 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADOConnection *pConnection) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
// EndEventExampleVC02 
```

<span data-ttu-id="2c04c-p103">Las clases de eventos heredan de **IUnknown**, por lo que también se deben implementar los métodos **QueryInterface**, **AddRef** y **Release**. Además, implemente constructores y destructores de clases. Elija las herramientas de Visual C++ que prefiera para simplificar esta parte de la tarea.</span><span class="sxs-lookup"><span data-stu-id="2c04c-p103">The event classes inherit from **IUnknown**, so you must also implement the **QueryInterface**, **AddRef**, and **Release** methods. Also implement class constructors and destructors. Choose the Visual C++ tools with which you are most comfortable to simplify this part of the task.</span></span>

<span data-ttu-id="2c04c-p104">Notifique la disponibilidad de sus controladores de eventos emitiendo una llamada a **QueryInterface** en los objetos [Recordset](recordset-object-ado.md) y [Connection](connection-object-ado.md) para las interfaces **IConnectionPointContainer** e **IConnectionPoint**. A continuación, emita **IConnectionPoint::Advise** para cada clase.</span><span class="sxs-lookup"><span data-stu-id="2c04c-p104">Make it known that your event handlers are available by issuing **QueryInterface** on the [Recordset](recordset-object-ado.md) and [Connection](connection-object-ado.md) objects for the **IConnectionPointContainer** and **IConnectionPoint** interfaces. Then issue **IConnectionPoint::Advise** for each class.</span></span>

<span data-ttu-id="2c04c-116">Por ejemplo, suponga que está usando una función booleana que devuelve **True** si informa correctamente a un objeto **Recordset** de que sus controladores de eventos están disponibles.</span><span class="sxs-lookup"><span data-stu-id="2c04c-116">For example, assume you are using a Boolean function that returns **True** if it successfully informs a **Recordset** object that you have event handlers available.</span></span>

```cpp 
 
// BeginEventExampleVC03 
HRESULT hr; 
DWORD dwEvtClass; 
IConnectionPointContainer *pCPC = NULL; 
IConnectionPoint *pCP = NULL; 
CRstEvent *pRStEvent = NULL; 
... 
_RecordsetPtr pRs; 
pRs.CreateInstance(__uuidof(Recordset)); 
pRStEvent = new CRstEvent; 
if (pRStEvent == NULL) return FALSE; 
... 
hr = pRs->QueryInterface(IID_IConnectionPointContainer, (LPVOID *)&pCPC); 
if (FAILED(hr)) return FALSE; 
hr = pCPC->FindConnectionPoint(RecordsetEvents, &pCP); 
pCPC->Release(); // Always Release now, even before checking. 
if (FAILED(hr)) return FALSE; 
hr = pCP->Advise(pRstEvent, &dwEvtClass); //Turn on event support. 
pCP->Release(); 
if (FAILED(hr)) return FALSE; 
... 
return TRUE; 
... 
// EndEventExampleVC03 
```

<span data-ttu-id="2c04c-117">En este punto, se habilitan eventos para la familia **RecordsetEvent** y sus métodos recibirán llamadas cuando se produzcan eventos de **conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="2c04c-117">At this point, events for the **RecordsetEvent** family are enabled and your methods will be called as **Recordset** events occur.</span></span>

<span data-ttu-id="2c04c-118">Más tarde, si desea que sus controladores de eventos dejen de estar disponibles, obtenga de nuevo el punto de conexión y emita el método **IConnectionPoint::Unadvise**.</span><span class="sxs-lookup"><span data-stu-id="2c04c-118">Later, when you want to make your event handlers unavailable, get the connection point again and issue the **IConnectionPoint::Unadvise** method.</span></span>

```cpp 
 
// BeginEventExampleVC04 
... 
hr = pCP->Unadvise(dwEvtClass); //Turn off event support. 
pCP->Release(); 
if (FAILED(hr)) return FALSE; 
... 
// EndEventExampleVC04 
```

<span data-ttu-id="2c04c-119">Debe liberar interfaces y destruir objetos de clase según proceda.</span><span class="sxs-lookup"><span data-stu-id="2c04c-119">You must release interfaces and destroy class objects as appropriate.</span></span>

<span data-ttu-id="2c04c-120">El código siguiente muestra un ejemplo completo de una clase de receptor de eventos de **conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="2c04c-120">The following code shows a complete example of a **Recordset** Event sink class.</span></span>

```vb 
 
// BeginEventExampleVC05 
#include <adoint.h> 
 
class CADORecordsetEvents : public RecordsetEventsVt 
{ 
public : 
 
 ULONG m_ulRefCount; 
 CADORecordsetEvents():m_ulRefCount(1){} 
 
 STDMETHOD(QueryInterface)(REFIID iid, LPVOID * ppvObject) 
 { 
 if (IsEqualIID(__uuidof(IUnknown), iid) || 
 IsEqualIID(__uuidof(RecordsetEventsVt), iid)) 
 { 
 *ppvObject = this; 
 return S_OK; 
 } 
 else 
 return E_NOINTERFACE; 
 } 
 
 STDMETHOD_(ULONG, AddRef)() 
 { 
 return m_ulRefCount++; 
 } 
 
 STDMETHOD_(ULONG, Release)() 
 { 
 if (--m_ulRefCount == 0) 
 { 
 delete this; 
 return 0; 
 } 
 else 
 return m_ulRefCount; 
 } 
 
 
 STDMETHOD(WillChangeField)( 
 LONG cFields, 
 VARIANT Fields, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(FieldChangeComplete)( 
 LONG cFields, 
 VARIANT Fields, 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(WillChangeRecord)( 
 EventReasonEnum adReason, 
 LONG cRecords, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(RecordChangeComplete)( 
 EventReasonEnum adReason, 
 LONG cRecords, 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(WillChangeRecordset)( 
 EventReasonEnum adReason, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(RecordsetChangeComplete)( 
 EventReasonEnum adReason, 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(WillMove)( 
 EventReasonEnum adReason, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(MoveComplete)( 
 EventReasonEnum adReason, 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(EndOfRecordset)( 
 VARIANT_BOOL *fMoreData, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(FetchProgress)( 
 long Progress, 
 long MaxProgress, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(FetchComplete)( 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
}; 
// EndEventExampleVC05 
```

