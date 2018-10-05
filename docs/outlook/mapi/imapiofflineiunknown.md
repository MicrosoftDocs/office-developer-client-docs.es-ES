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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401282"
---
# <a name="imapioffline--iunknown"></a><span data-ttu-id="5b10e-103">IMAPIOffline : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5b10e-103">IMAPIOffline : IUnknown</span></span>

  
  
<span data-ttu-id="5b10e-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b10e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b10e-105">Proporciona información de un objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="5b10e-105">Provides information for an offline object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5b10e-106">Suministrado por:</span><span class="sxs-lookup"><span data-stu-id="5b10e-106">Provided by:</span></span>  <br/> |<span data-ttu-id="5b10e-107">Consulta en [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)</span><span class="sxs-lookup"><span data-stu-id="5b10e-107">Query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)</span></span> <br/> |
|<span data-ttu-id="5b10e-108">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="5b10e-108">Called by:</span></span>  <br/> |<span data-ttu-id="5b10e-109">Cliente</span><span class="sxs-lookup"><span data-stu-id="5b10e-109">Client</span></span>  <br/> |
|<span data-ttu-id="5b10e-110">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="5b10e-110">Interface identifier:</span></span>  <br/> |<span data-ttu-id="5b10e-111">IID_IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="5b10e-111">IID_IMAPIOffline</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="5b10e-112">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="5b10e-112">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5b10e-113">**[SetCurrentState](imapioffline-setcurrentstate.md)**</span><span class="sxs-lookup"><span data-stu-id="5b10e-113">**[SetCurrentState](imapioffline-setcurrentstate.md)**</span></span> <br/> |<span data-ttu-id="5b10e-114">Establece el estado actual de un objeto sin conexión a en línea o sin conexión.</span><span class="sxs-lookup"><span data-stu-id="5b10e-114">Sets the current state of an offline object to online or offline.</span></span>  <br/> |
|<span data-ttu-id="5b10e-115">**[GetCapabilities](imapioffline-getcapabilities.md)**</span><span class="sxs-lookup"><span data-stu-id="5b10e-115">**[GetCapabilities](imapioffline-getcapabilities.md)**</span></span> <br/> |<span data-ttu-id="5b10e-116">Obtiene las condiciones para la que se admiten las devoluciones de llamada por un objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="5b10e-116">Gets the conditions for which callbacks are supported by an offline object.</span></span>  <br/> |
|<span data-ttu-id="5b10e-117">**[GetCurrentState](imapioffline-getcurrentstate.md)**</span><span class="sxs-lookup"><span data-stu-id="5b10e-117">**[GetCurrentState](imapioffline-getcurrentstate.md)**</span></span> <br/> |<span data-ttu-id="5b10e-118">Obtiene el estado en línea o sin conexión actual de un objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="5b10e-118">Gets the current online or offline state of an offline object.</span></span>  <br/> |
| <span data-ttu-id="5b10e-119">*Miembro de marcador de posición*</span><span class="sxs-lookup"><span data-stu-id="5b10e-119">*Placeholder member*</span></span>  <br/> |<span data-ttu-id="5b10e-120">Este miembro es un marcador de posición y no se admite.</span><span class="sxs-lookup"><span data-stu-id="5b10e-120">This member is a placeholder and is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b10e-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5b10e-121">Remarks</span></span>

<span data-ttu-id="5b10e-122">Un cliente usa **[HrOpenOfflineObj](hropenofflineobj.md)** para abrir y obtener un objeto sin conexión que admite **IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="5b10e-122">A client uses **[HrOpenOfflineObj](hropenofflineobj.md)** to open and obtain an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="5b10e-123">Debido a que **IMAPIOfflineMgr** hereda de [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx), el cliente puede consultar esta interfaz (mediante el uso de [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)) para obtener un puntero al puntero de interfaz para **IMAPIOffline** para el objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="5b10e-123">Because **IMAPIOfflineMgr** inherits from [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx), the client can query this interface (by using [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)) to obtain a pointer to the interface pointer for **IMAPIOffline** for the offline object.</span></span> <span data-ttu-id="5b10e-124">El cliente puede, a continuación, obtener o establecer el estado actual del objeto, u Obtenga información acerca de las funciones de devolución de llamada del objeto (mediante una llamada a **IMAPIOffline::GetCapabilities** ) y elija Configurar las devoluciones de llamada mediante el uso de **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span><span class="sxs-lookup"><span data-stu-id="5b10e-124">The client can then get or set the current state of the object, or find out about the callback capabilities of the object (by calling **IMAPIOffline::GetCapabilities** ) and choose to set up callbacks by using **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span></span> 
  
<span data-ttu-id="5b10e-125">Un miembro de esta interfaz es un marcador de posición reservado para el uso interno de Microsoft Outlook 2013 y está sujeta a cambios.</span><span class="sxs-lookup"><span data-stu-id="5b10e-125">A member in this interface is a placeholder reserved for the internal use of Microsoft Outlook 2013 and is subject to change.</span></span> <span data-ttu-id="5b10e-126">Otros miembros de esta interfaz deben usarse sólo como se indica.</span><span class="sxs-lookup"><span data-stu-id="5b10e-126">Other members in this interface must be used only as documented.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5b10e-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b10e-127">See also</span></span>



[<span data-ttu-id="5b10e-128">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="5b10e-128">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="5b10e-129">Información sobre la API de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="5b10e-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="5b10e-130">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="5b10e-130">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="5b10e-131">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="5b10e-131">MAPI Interfaces</span></span>](mapi-interfaces.md)

