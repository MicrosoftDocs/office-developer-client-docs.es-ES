---
title: Los eventos disponibles y su identificadores DispId (API exportadas de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1fd848c7-038e-4e2f-8997-c8509b31df79
description: En esta sección se describe los identificadores de envío para los eventos que Outlook pone a disposición.
ms.openlocfilehash: 1542ff85579346a3674593e9ea38115170df2237
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816066"
---
# <a name="available-events-and-their-dispids-outlook-exported-apis"></a><span data-ttu-id="2b0dc-103">Los eventos disponibles y su identificadores DispId (API exportadas de Outlook)</span><span class="sxs-lookup"><span data-stu-id="2b0dc-103">Available events and their dispids (Outlook exported APIs)</span></span>

<span data-ttu-id="2b0dc-104">En esta sección se describe los identificadores de envío para los eventos que Outlook pone a disposición.</span><span class="sxs-lookup"><span data-stu-id="2b0dc-104">This section describes the dispatch identifiers for the events that Outlook makes available.</span></span>
  
<span data-ttu-id="2b0dc-105">Outlook expone los siguientes identificadores de envío (DISPID) para permitir que los complementos de C++ escuchar y controlar los eventos correspondientes de la función de [IDispatch:: Invoke](http://msdn.microsoft.com/library/automat.idispatch_invoke%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2b0dc-105">Outlook exposes the following dispatch identifiers (dispids) to allow C++ add-ins to listen to and handle the corresponding events from the [IDispatch::Invoke](http://msdn.microsoft.com/library/automat.idispatch_invoke%28Office.15%29.aspx) function.</span></span> 
  
|<span data-ttu-id="2b0dc-106">**Constante**</span><span class="sxs-lookup"><span data-stu-id="2b0dc-106">**Constant**</span></span>|<span data-ttu-id="2b0dc-107">**Identificador de envío (evento)**</span><span class="sxs-lookup"><span data-stu-id="2b0dc-107">**Dispid for event**</span></span>|<span data-ttu-id="2b0dc-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2b0dc-108">**Description**</span></span>|<span data-ttu-id="2b0dc-109">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="2b0dc-109">**Parameters**</span></span>|<span data-ttu-id="2b0dc-110">**Comentarios**</span><span class="sxs-lookup"><span data-stu-id="2b0dc-110">**Remarks**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2b0dc-111">**dispidBeforePrint**</span><span class="sxs-lookup"><span data-stu-id="2b0dc-111">**dispidBeforePrint**</span></span> <br/> |<span data-ttu-id="2b0dc-112">0xFC8E</span><span class="sxs-lookup"><span data-stu-id="2b0dc-112">0xFC8E</span></span>  <br/> |<span data-ttu-id="2b0dc-113">Se usa para controlar el evento de nivel de la aplicación de la función de **IDispatch:: Invoke** que se desencadena antes de una operación de impresión.</span><span class="sxs-lookup"><span data-stu-id="2b0dc-113">Used to handle the application-level event from the **IDispatch::Invoke** function that fires before a printing operation.</span></span>  <br/> | <span data-ttu-id="2b0dc-114">Hay 2 parámetros sin nombre:</span><span class="sxs-lookup"><span data-stu-id="2b0dc-114">There are 2 unnamed parameters:</span></span>  <br/>  <span data-ttu-id="2b0dc-115">El primer parámetro es del tipo ** VT_BOOL</span><span class="sxs-lookup"><span data-stu-id="2b0dc-115">The first parameter is of the type **VT_BOOL</span></span>|<span data-ttu-id="2b0dc-116">VT_BREF **.</span><span class="sxs-lookup"><span data-stu-id="2b0dc-116">VT_BREF**.</span></span> <span data-ttu-id="2b0dc-117">Devolver **VARIANT_TRUE** en este parámetro para cancelar el evento.</span><span class="sxs-lookup"><span data-stu-id="2b0dc-117">Return **VARIANT_TRUE** in this parameter to cancel the event.</span></span>  <br/>  <span data-ttu-id="2b0dc-118">El segundo parámetro no se utiliza y se debe omitir.</span><span class="sxs-lookup"><span data-stu-id="2b0dc-118">The second parameter is not used and should be ignored.</span></span>  <br/> |<span data-ttu-id="2b0dc-119">Este dispid está disponible desde Outlook 2010.</span><span class="sxs-lookup"><span data-stu-id="2b0dc-119">This dispid is available since Outlook 2010.</span></span>  <br/> |
|<span data-ttu-id="2b0dc-120">**dispidEventReadComplete**</span><span class="sxs-lookup"><span data-stu-id="2b0dc-120">**dispidEventReadComplete**</span></span> <br/> |<span data-ttu-id="2b0dc-121">0xFC8F</span><span class="sxs-lookup"><span data-stu-id="2b0dc-121">0xFC8F</span></span>  <br/> |<span data-ttu-id="2b0dc-122">Se usa para controlar el evento de nivel de elemento de la función de **IDispatch:: Invoke** que se desencadena cuando Outlook ha finalizado la lectura de las propiedades del elemento.</span><span class="sxs-lookup"><span data-stu-id="2b0dc-122">Used to handle the item-level event from the **IDispatch::Invoke** function that fires when Outlook has completed reading the properties of the item.</span></span>  <br/> |<span data-ttu-id="2b0dc-123">Hay un solo parámetro _Cancelar_ que es del tipo ** VT_BOOL</span><span class="sxs-lookup"><span data-stu-id="2b0dc-123">There is only one parameter  _Cancel_ which is of the type **VT_BOOL</span></span>|<span data-ttu-id="2b0dc-124">VT_BREF **.</span><span class="sxs-lookup"><span data-stu-id="2b0dc-124">VT_BREF**.</span></span> <span data-ttu-id="2b0dc-125">Devolver **VARIANT_TRUE** en este parámetro para cancelar la operación de lectura.</span><span class="sxs-lookup"><span data-stu-id="2b0dc-125">Return **VARIANT_TRUE** in this parameter to cancel the read operation.</span></span>  <br/> |<span data-ttu-id="2b0dc-126">Este dispid está disponible desde Outlook 2010.</span><span class="sxs-lookup"><span data-stu-id="2b0dc-126">This dispid is available since Outlook 2010.</span></span>  <br/> <span data-ttu-id="2b0dc-127">Este evento corresponde al evento las extensiones de cliente de Exchange (ECE) **IExchExtMessageEvents::OnReadComplete**, y también para el evento **ReadComplete** que se ha agregado al modelo de objetos desde Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="2b0dc-127">This event corresponds to the Exchange Client Extensions (ECE) event **IExchExtMessageEvents::OnReadComplete**, and also to the **ReadComplete** event that has been added to the object model since Outlook 2013.</span></span>  <br/> |
   
<span data-ttu-id="2b0dc-128">Para obtener un ejemplo de cómo usar un dispid para escuchar y controlar un evento, vea el `CAppEventListener::Invoke` (función) en la solución de Outlook de C++ se describe en [Implementar receptores de eventos de Outlook 2002/XP en MFC C++ 2003. NET](http://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C).</span><span class="sxs-lookup"><span data-stu-id="2b0dc-128">For an example of how to use a dispid to listen to and handle an event, see the  `CAppEventListener::Invoke` function in the C++ Outlook solution described in [Implementing Outlook 2002/XP Event Sinks in MFC C++ 2003 .NET](http://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2b0dc-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b0dc-129">See also</span></span>

- [<span data-ttu-id="2b0dc-130">API exportadas de Outlook</span><span class="sxs-lookup"><span data-stu-id="2b0dc-130">Outlook exported APIs</span></span>](outlook-exported-apis.md)
- [<span data-ttu-id="2b0dc-131">Constantes (API exportadas de Outlook)</span><span class="sxs-lookup"><span data-stu-id="2b0dc-131">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="2b0dc-132">Información sobre las API exportadas por Outlook</span><span class="sxs-lookup"><span data-stu-id="2b0dc-132">About APIs exported by Outlook</span></span>](about-apis-exported-by-outlook.md)
- [<span data-ttu-id="2b0dc-133">Implementar eventos de Outlook 2002/XP receptores en MFC C++ .NET 2003</span><span class="sxs-lookup"><span data-stu-id="2b0dc-133">Implementing Outlook 2002/XP Event Sinks in MFC C++ 2003 .NET</span></span>](http://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C)
