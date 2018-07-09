---
title: IMAPIOffline IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline
api_type:
- COM
ms.assetid: 211281ff-3c22-1b51-4b72-ca1e313c7202
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 6f17e501a90a50a4984cae470d3924205c78a604
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817391"
---
# <a name="imapioffline--iunknown"></a><span data-ttu-id="40c35-103">IMAPIOffline: IUnknown</span><span class="sxs-lookup"><span data-stu-id="40c35-103">IMAPIOffline : IUnknown</span></span>

  
  
<span data-ttu-id="40c35-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="40c35-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="40c35-105">Proporciona información de un objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="40c35-105">Provides information for an offline object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="40c35-106">Suministrado por:</span><span class="sxs-lookup"><span data-stu-id="40c35-106">Provided by:</span></span>  <br/> |<span data-ttu-id="40c35-107">Consulta en [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)</span><span class="sxs-lookup"><span data-stu-id="40c35-107">Query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)</span></span> <br/> |
|<span data-ttu-id="40c35-108">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="40c35-108">Called by:</span></span>  <br/> |<span data-ttu-id="40c35-109">Cliente</span><span class="sxs-lookup"><span data-stu-id="40c35-109">Client</span></span>  <br/> |
|<span data-ttu-id="40c35-110">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="40c35-110">Interface identifier:</span></span>  <br/> |<span data-ttu-id="40c35-111">IID_IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="40c35-111">IID_IMAPIOffline</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="40c35-112">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="40c35-112">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="40c35-113">**[SetCurrentState](imapioffline-setcurrentstate.md)**</span><span class="sxs-lookup"><span data-stu-id="40c35-113">**[SetCurrentState](imapioffline-setcurrentstate.md)**</span></span> <br/> |<span data-ttu-id="40c35-114">Establece el estado actual de un objeto sin conexión a en línea o sin conexión.</span><span class="sxs-lookup"><span data-stu-id="40c35-114">Sets the current state of an offline object to online or offline.</span></span>  <br/> |
|<span data-ttu-id="40c35-115">**[GetCapabilities](imapioffline-getcapabilities.md)**</span><span class="sxs-lookup"><span data-stu-id="40c35-115">**[GetCapabilities](imapioffline-getcapabilities.md)**</span></span> <br/> |<span data-ttu-id="40c35-116">Obtiene las condiciones para la que se admiten las devoluciones de llamada por un objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="40c35-116">Gets the conditions for which callbacks are supported by an offline object.</span></span>  <br/> |
|<span data-ttu-id="40c35-117">**[GetCurrentState](imapioffline-getcurrentstate.md)**</span><span class="sxs-lookup"><span data-stu-id="40c35-117">**[GetCurrentState](imapioffline-getcurrentstate.md)**</span></span> <br/> |<span data-ttu-id="40c35-118">Obtiene el estado en línea o sin conexión actual de un objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="40c35-118">Gets the current online or offline state of an offline object.</span></span>  <br/> |
| <span data-ttu-id="40c35-119">*Miembro de marcador de posición*</span><span class="sxs-lookup"><span data-stu-id="40c35-119">*Placeholder member*</span></span>  <br/> |<span data-ttu-id="40c35-120">Este miembro es un marcador de posición y no se admite.</span><span class="sxs-lookup"><span data-stu-id="40c35-120">This member is a placeholder and is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40c35-121">Notas</span><span class="sxs-lookup"><span data-stu-id="40c35-121">Remarks</span></span>

<span data-ttu-id="40c35-122">Un cliente usa **[HrOpenOfflineObj](hropenofflineobj.md)** para abrir y obtener un objeto sin conexión que admite **IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="40c35-122">A client uses **[HrOpenOfflineObj](hropenofflineobj.md)** to open and obtain an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="40c35-123">Debido a que **IMAPIOfflineMgr** hereda de [IUnknown](http://msdn.microsoft.com/es-es/library/ms680509%28v=VS.85%29.aspx), el cliente puede consultar esta interfaz (mediante el uso de [IUnknown:: QueryInterface](http://msdn.microsoft.com/es-es/library/ms682521%28v=VS.85%29.aspx)) para obtener un puntero al puntero de interfaz para **IMAPIOffline** para el objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="40c35-123">Because **IMAPIOfflineMgr** inherits from [IUnknown](http://msdn.microsoft.com/es-es/library/ms680509%28v=VS.85%29.aspx), the client can query this interface (by using [IUnknown::QueryInterface](http://msdn.microsoft.com/es-es/library/ms682521%28v=VS.85%29.aspx)) to obtain a pointer to the interface pointer for **IMAPIOffline** for the offline object.</span></span> <span data-ttu-id="40c35-124">El cliente puede, a continuación, obtener o establecer el estado actual del objeto, u Obtenga información acerca de las funciones de devolución de llamada del objeto (mediante una llamada a **IMAPIOffline::GetCapabilities** ) y elija Configurar las devoluciones de llamada mediante el uso de **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span><span class="sxs-lookup"><span data-stu-id="40c35-124">The client can then get or set the current state of the object, or find out about the callback capabilities of the object (by calling **IMAPIOffline::GetCapabilities** ) and choose to set up callbacks by using **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span></span> 
  
<span data-ttu-id="40c35-125">Un miembro de esta interfaz es un marcador de posición reservado para el uso interno de Microsoft Outlook 2013 y está sujeta a cambios.</span><span class="sxs-lookup"><span data-stu-id="40c35-125">A member in this interface is a placeholder reserved for the internal use of Microsoft Outlook 2013 and is subject to change.</span></span> <span data-ttu-id="40c35-126">Otros miembros de esta interfaz deben usarse sólo como se indica.</span><span class="sxs-lookup"><span data-stu-id="40c35-126">Other members in this interface must be used only as documented.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="40c35-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="40c35-127">See also</span></span>



[<span data-ttu-id="40c35-128">IMAPIOfflineMgr: IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="40c35-128">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="40c35-129">Acerca de la API de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="40c35-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="40c35-130">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="40c35-130">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="40c35-131">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="40c35-131">MAPI Interfaces</span></span>](mapi-interfaces.md)

