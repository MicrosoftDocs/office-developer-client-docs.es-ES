---
title: IXPProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPProvider
api_type:
- COM
ms.assetid: d5507785-c924-4981-ae80-19709ceb054d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 49cb500279540317059cde2d9baba28fcbf06165
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574114"
---
# <a name="ixpprovider--iunknown"></a><span data-ttu-id="a186a-103">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a186a-103">IXPProvider : IUnknown</span></span>

  
  
<span data-ttu-id="a186a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a186a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a186a-105">Inicializa un objeto de proveedor de transporte y se cierra el objeto cuando ya no sea necesaria.</span><span class="sxs-lookup"><span data-stu-id="a186a-105">Initializes a transport provider object and shuts down the object when it is no longer needed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a186a-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="a186a-106">Header file:</span></span>  <br/> |<span data-ttu-id="a186a-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="a186a-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="a186a-108">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="a186a-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="a186a-109">Objetos de proveedor de transporte</span><span class="sxs-lookup"><span data-stu-id="a186a-109">Transport provider objects</span></span>  <br/> |
|<span data-ttu-id="a186a-110">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="a186a-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="a186a-111">Proveedores de transporte</span><span class="sxs-lookup"><span data-stu-id="a186a-111">Transport providers</span></span>  <br/> |
|<span data-ttu-id="a186a-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="a186a-112">Called by:</span></span>  <br/> |<span data-ttu-id="a186a-113">La cola MAPI</span><span class="sxs-lookup"><span data-stu-id="a186a-113">The MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="a186a-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="a186a-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a186a-115">IID_IXPProvider</span><span class="sxs-lookup"><span data-stu-id="a186a-115">IID_IXPProvider</span></span>  <br/> |
|<span data-ttu-id="a186a-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="a186a-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="a186a-117">LPXPROVIDER</span><span class="sxs-lookup"><span data-stu-id="a186a-117">LPXPROVIDER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a186a-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="a186a-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a186a-119">Apagado</span><span class="sxs-lookup"><span data-stu-id="a186a-119">Shutdown</span></span>](ixpprovider-shutdown.md) <br/> |<span data-ttu-id="a186a-120">Se cierra un proveedor de transporte de una forma ordenada.</span><span class="sxs-lookup"><span data-stu-id="a186a-120">Closes down a transport provider in an orderly fashion.</span></span>  <br/> |
|[<span data-ttu-id="a186a-121">TransportLogon</span><span class="sxs-lookup"><span data-stu-id="a186a-121">TransportLogon</span></span>](ixpprovider-transportlogon.md) <br/> |<span data-ttu-id="a186a-122">Establece una sesión en el que una aplicación cliente inicia sesión en un proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="a186a-122">Establishes a session in which a client application logs on to a transport provider.</span></span>  <br/> |
   

