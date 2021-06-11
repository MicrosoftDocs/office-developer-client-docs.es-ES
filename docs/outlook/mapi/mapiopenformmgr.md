---
title: MAPIOpenFormMgr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIOpenFormMgr
api_type:
- COM
ms.assetid: 5b624954-d975-4d5e-84d7-74e096ac30af
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: de0c1181450c536dffd5a84242c17bd1dd612566
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418053"
---
# <a name="mapiopenformmgr"></a><span data-ttu-id="7b5c3-103">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="7b5c3-103">MAPIOpenFormMgr</span></span>

  
  
<span data-ttu-id="7b5c3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b5c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b5c3-105">Abre una [interfaz IMAPIFormMgr](imapiformmgriunknown.md) en un objeto de proveedor de biblioteca de formularios en el contexto de una sesión existente.</span><span class="sxs-lookup"><span data-stu-id="7b5c3-105">Opens an [IMAPIFormMgr](imapiformmgriunknown.md) interface on a form library provider object in the context of an existing session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7b5c3-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="7b5c3-106">Header file:</span></span>  <br/> |<span data-ttu-id="7b5c3-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="7b5c3-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="7b5c3-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="7b5c3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7b5c3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7b5c3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7b5c3-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="7b5c3-110">Called by:</span></span>  <br/> |<span data-ttu-id="7b5c3-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="7b5c3-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenFormMgr(
  LPMAPISESSION pSession,
  LPMAPIFORMMGR FAR * ppmgr
);
```

## <a name="parameters"></a><span data-ttu-id="7b5c3-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="7b5c3-112">Parameters</span></span>

 <span data-ttu-id="7b5c3-113">_pSession_</span><span class="sxs-lookup"><span data-stu-id="7b5c3-113">_pSession_</span></span>
  
> <span data-ttu-id="7b5c3-114">[in] Puntero a la sesión en uso por la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="7b5c3-114">[in] Pointer to the session in use by the client application.</span></span>
    
 <span data-ttu-id="7b5c3-115">_ppmgr_</span><span class="sxs-lookup"><span data-stu-id="7b5c3-115">_ppmgr_</span></span>
  
> <span data-ttu-id="7b5c3-116">[salida] Puntero a la interfaz **IMAPIFormMgr** devuelta.</span><span class="sxs-lookup"><span data-stu-id="7b5c3-116">[out] Pointer to the returned **IMAPIFormMgr** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7b5c3-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7b5c3-117">Return value</span></span>

<span data-ttu-id="7b5c3-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7b5c3-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7b5c3-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7b5c3-119">Remarks</span></span>

<span data-ttu-id="7b5c3-120">Después de que una aplicación cliente realiza una llamada a la función **MAPIOpenFormMgr,** la mayoría de las interacciones relacionadas con formularios posteriores tienen lugar a través del proveedor de biblioteca de formularios o una interfaz devuelta por el proveedor de bibliotecas de formularios.</span><span class="sxs-lookup"><span data-stu-id="7b5c3-120">After a client application makes a call to the **MAPIOpenFormMgr** function, most subsequent forms-related interactions take place through the form library provider or an interface returned by the form library provider.</span></span> <span data-ttu-id="7b5c3-121">La **interfaz IMAPIFormMgr** permite al cliente trabajar con controladores de mensajes y realizar resoluciones entre clases de mensajes y bibliotecas de formularios.</span><span class="sxs-lookup"><span data-stu-id="7b5c3-121">The **IMAPIFormMgr** interface allows the client to work with message handlers and perform resolutions between message classes and form libraries.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7b5c3-122">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7b5c3-122">MFCMAPI reference</span></span>

<span data-ttu-id="7b5c3-123">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="7b5c3-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7b5c3-124">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="7b5c3-124">**File**</span></span>|<span data-ttu-id="7b5c3-125">**Función**</span><span class="sxs-lookup"><span data-stu-id="7b5c3-125">**Function**</span></span>|<span data-ttu-id="7b5c3-126">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="7b5c3-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7b5c3-127">MainDlg.cpp abre el administrador de formularios para que se pueda seleccionar un formulario.</span><span class="sxs-lookup"><span data-stu-id="7b5c3-127">MainDlg.cpp opens the form manager so a form can be selected.</span></span>  <br/> |<span data-ttu-id="7b5c3-128">CMainDlg::OnSelectForm</span><span class="sxs-lookup"><span data-stu-id="7b5c3-128">CMainDlg::OnSelectForm</span></span>  <br/> |<span data-ttu-id="7b5c3-129">MFCMAPI usa el **método MAPIOpenFormMgr** para abrir el administrador de formularios para que se pueda seleccionar un formulario.</span><span class="sxs-lookup"><span data-stu-id="7b5c3-129">MFCMAPI uses the **MAPIOpenFormMgr** method to open the form manager so a form can be selected.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7b5c3-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b5c3-130">See also</span></span>



[<span data-ttu-id="7b5c3-131">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="7b5c3-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

