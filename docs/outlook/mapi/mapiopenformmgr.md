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
ms.openlocfilehash: 592bd2c88c8eea17d80fe7cb725b075235c51763
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818259"
---
# <a name="mapiopenformmgr"></a><span data-ttu-id="ca0e6-103">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="ca0e6-103">MAPIOpenFormMgr</span></span>

  
  
<span data-ttu-id="ca0e6-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ca0e6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ca0e6-105">Se abre una interfaz [IMAPIFormMgr](imapiformmgriunknown.md) en un objeto de proveedor de la biblioteca de formulario en el contexto de una sesión existente.</span><span class="sxs-lookup"><span data-stu-id="ca0e6-105">Opens an [IMAPIFormMgr](imapiformmgriunknown.md) interface on a form library provider object in the context of an existing session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ca0e6-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="ca0e6-106">Header file:</span></span>  <br/> |<span data-ttu-id="ca0e6-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="ca0e6-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="ca0e6-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="ca0e6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ca0e6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ca0e6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ca0e6-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="ca0e6-110">Called by:</span></span>  <br/> |<span data-ttu-id="ca0e6-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="ca0e6-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenFormMgr(
  LPMAPISESSION pSession,
  LPMAPIFORMMGR FAR * ppmgr
);
```

## <a name="parameters"></a><span data-ttu-id="ca0e6-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ca0e6-112">Parameters</span></span>

 <span data-ttu-id="ca0e6-113">_pSession_</span><span class="sxs-lookup"><span data-stu-id="ca0e6-113">_pSession_</span></span>
  
> <span data-ttu-id="ca0e6-114">[entrada] Puntero a la sesión en uso por la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="ca0e6-114">[in] Pointer to the session in use by the client application.</span></span>
    
 <span data-ttu-id="ca0e6-115">_ppmgr_</span><span class="sxs-lookup"><span data-stu-id="ca0e6-115">_ppmgr_</span></span>
  
> <span data-ttu-id="ca0e6-116">[out] Puntero a la interfaz devuelta de **IMAPIFormMgr** .</span><span class="sxs-lookup"><span data-stu-id="ca0e6-116">[out] Pointer to the returned **IMAPIFormMgr** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ca0e6-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ca0e6-117">Return value</span></span>

<span data-ttu-id="ca0e6-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ca0e6-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ca0e6-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ca0e6-119">Remarks</span></span>

<span data-ttu-id="ca0e6-120">Después de que una aplicación cliente realiza una llamada a la función **MAPIOpenFormMgr** , la mayoría relacionadas con formularios de las interacciones subsiguientes tienen lugar a través de una interfaz devuelto por el proveedor de la biblioteca de formulario o el proveedor de la biblioteca de formulario.</span><span class="sxs-lookup"><span data-stu-id="ca0e6-120">After a client application makes a call to the **MAPIOpenFormMgr** function, most subsequent forms-related interactions take place through the form library provider or an interface returned by the form library provider.</span></span> <span data-ttu-id="ca0e6-121">La interfaz de **IMAPIFormMgr** permite que el cliente trabajar con controladores de mensajes y realizar resoluciones entre las clases de mensajes y las bibliotecas de formularios.</span><span class="sxs-lookup"><span data-stu-id="ca0e6-121">The **IMAPIFormMgr** interface allows the client to work with message handlers and perform resolutions between message classes and form libraries.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ca0e6-122">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ca0e6-122">MFCMAPI reference</span></span>

<span data-ttu-id="ca0e6-123">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="ca0e6-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ca0e6-124">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="ca0e6-124">**File**</span></span>|<span data-ttu-id="ca0e6-125">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="ca0e6-125">**Function**</span></span>|<span data-ttu-id="ca0e6-126">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="ca0e6-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ca0e6-127">MainDlg.cpp abre el Administrador de formularios de modo que se puede seleccionar un formulario.</span><span class="sxs-lookup"><span data-stu-id="ca0e6-127">MainDlg.cpp opens the form manager so a form can be selected.</span></span>  <br/> |<span data-ttu-id="ca0e6-128">CMainDlg::OnSelectForm</span><span class="sxs-lookup"><span data-stu-id="ca0e6-128">CMainDlg::OnSelectForm</span></span>  <br/> |<span data-ttu-id="ca0e6-129">MFCMAPI usa el método **MAPIOpenFormMgr** para abrir el Administrador de formulario, por lo que se puede seleccionar un formulario.</span><span class="sxs-lookup"><span data-stu-id="ca0e6-129">MFCMAPI uses the **MAPIOpenFormMgr** method to open the form manager so a form can be selected.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ca0e6-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca0e6-130">See also</span></span>



[<span data-ttu-id="ca0e6-131">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="ca0e6-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

