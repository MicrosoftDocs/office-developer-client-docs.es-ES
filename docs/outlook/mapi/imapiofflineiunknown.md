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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 20d8c39765b0dbbfdde530361894d0a27876010a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321269"
---
# <a name="imapioffline--iunknown"></a><span data-ttu-id="14aa9-103">IMAPIOffline : IUnknown</span><span class="sxs-lookup"><span data-stu-id="14aa9-103">IMAPIOffline : IUnknown</span></span>

  
  
<span data-ttu-id="14aa9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="14aa9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="14aa9-105">Proporciona información para un objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="14aa9-105">Provides information for an offline object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="14aa9-106">Suministrado por:</span><span class="sxs-lookup"><span data-stu-id="14aa9-106">Provided by:</span></span>  <br/> |<span data-ttu-id="14aa9-107">Consulta en [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)</span><span class="sxs-lookup"><span data-stu-id="14aa9-107">Query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)</span></span> <br/> |
|<span data-ttu-id="14aa9-108">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="14aa9-108">Called by:</span></span>  <br/> |<span data-ttu-id="14aa9-109">Cliente</span><span class="sxs-lookup"><span data-stu-id="14aa9-109">Client</span></span>  <br/> |
|<span data-ttu-id="14aa9-110">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="14aa9-110">Interface identifier:</span></span>  <br/> |<span data-ttu-id="14aa9-111">IID_IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="14aa9-111">IID_IMAPIOffline</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="14aa9-112">Orden de Vtable</span><span class="sxs-lookup"><span data-stu-id="14aa9-112">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="14aa9-113">**[SetCurrentState](imapioffline-setcurrentstate.md)**</span><span class="sxs-lookup"><span data-stu-id="14aa9-113">**[SetCurrentState](imapioffline-setcurrentstate.md)**</span></span> <br/> |<span data-ttu-id="14aa9-114">Establece el estado actual de un objeto sin conexión en línea o sin conexión.</span><span class="sxs-lookup"><span data-stu-id="14aa9-114">Sets the current state of an offline object to online or offline.</span></span>  <br/> |
|<span data-ttu-id="14aa9-115">**[GetCapabilities](imapioffline-getcapabilities.md)**</span><span class="sxs-lookup"><span data-stu-id="14aa9-115">**[GetCapabilities](imapioffline-getcapabilities.md)**</span></span> <br/> |<span data-ttu-id="14aa9-116">Obtiene las condiciones para las que un objeto sin conexión admite las devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="14aa9-116">Gets the conditions for which callbacks are supported by an offline object.</span></span>  <br/> |
|<span data-ttu-id="14aa9-117">**[GetCurrentState](imapioffline-getcurrentstate.md)**</span><span class="sxs-lookup"><span data-stu-id="14aa9-117">**[GetCurrentState](imapioffline-getcurrentstate.md)**</span></span> <br/> |<span data-ttu-id="14aa9-118">Obtiene el estado actual en línea o sin conexión de un objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="14aa9-118">Gets the current online or offline state of an offline object.</span></span>  <br/> |
| <span data-ttu-id="14aa9-119">*Miembro de marcador de posición*</span><span class="sxs-lookup"><span data-stu-id="14aa9-119">*Placeholder member*</span></span>  <br/> |<span data-ttu-id="14aa9-120">Este miembro es un marcador de posición y no se admite.</span><span class="sxs-lookup"><span data-stu-id="14aa9-120">This member is a placeholder and is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="14aa9-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="14aa9-121">Remarks</span></span>

<span data-ttu-id="14aa9-122">Un cliente usa **[HrOpenOfflineObj para](hropenofflineobj.md)** abrir y obtener un objeto sin conexión compatible con **IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="14aa9-122">A client uses **[HrOpenOfflineObj](hropenofflineobj.md)** to open and obtain an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="14aa9-123">Dado que **IMAPIOfflineMgr** hereda de [IUnknown,](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)el cliente puede consultar esta interfaz (mediante [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)) para obtener un puntero al puntero de interfaz de **IMAPIOffline** para el objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="14aa9-123">Because **IMAPIOfflineMgr** inherits from [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx), the client can query this interface (by using [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)) to obtain a pointer to the interface pointer for **IMAPIOffline** for the offline object.</span></span> <span data-ttu-id="14aa9-124">A continuación, el cliente puede obtener o establecer el estado actual del objeto, o averiguar las capacidades de devolución de llamada del objeto (llamando a **IMAPIOffline::GetCapabilities** ) y elegir configurar las devoluciones de llamada mediante **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span><span class="sxs-lookup"><span data-stu-id="14aa9-124">The client can then get or set the current state of the object, or find out about the callback capabilities of the object (by calling **IMAPIOffline::GetCapabilities** ) and choose to set up callbacks by using **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span></span> 
  
<span data-ttu-id="14aa9-125">Un miembro de esta interfaz es un marcador de posición reservado para el uso interno de Microsoft Outlook 2013 y está sujeto a cambios.</span><span class="sxs-lookup"><span data-stu-id="14aa9-125">A member in this interface is a placeholder reserved for the internal use of Microsoft Outlook 2013 and is subject to change.</span></span> <span data-ttu-id="14aa9-126">Otros miembros de esta interfaz deben usarse solo como documentados.</span><span class="sxs-lookup"><span data-stu-id="14aa9-126">Other members in this interface must be used only as documented.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="14aa9-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="14aa9-127">See also</span></span>



[<span data-ttu-id="14aa9-128">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="14aa9-128">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="14aa9-129">Información sobre la API de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="14aa9-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="14aa9-130">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="14aa9-130">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="14aa9-131">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="14aa9-131">MAPI Interfaces</span></span>](mapi-interfaces.md)

