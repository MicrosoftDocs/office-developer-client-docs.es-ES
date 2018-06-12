---
title: MAPIOpenLocalFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIOpenLocalFormContainer
api_type:
- COM
ms.assetid: 1c53170f-03a6-4a05-913e-de8eeadea692
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: c00c2fa04ae7e89f8c23c085ba021a935748ad4e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818277"
---
# <a name="mapiopenlocalformcontainer"></a><span data-ttu-id="e690f-103">MAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="e690f-103">MAPIOpenLocalFormContainer</span></span>

  
  
<span data-ttu-id="e690f-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e690f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e690f-105">Devuelve un puntero de interfaz a la biblioteca de formularios local.</span><span class="sxs-lookup"><span data-stu-id="e690f-105">Returns an interface pointer to the local form library.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e690f-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e690f-106">Header file:</span></span>  <br/> |<span data-ttu-id="e690f-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="e690f-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="e690f-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="e690f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e690f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e690f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e690f-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="e690f-110">Called by:</span></span>  <br/> |<span data-ttu-id="e690f-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="e690f-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenLocalFormContainer(
  LPMAPIFORMCONTAINER FAR * ppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="e690f-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e690f-112">Parameters</span></span>

 <span data-ttu-id="e690f-113">_ppfcnt_</span><span class="sxs-lookup"><span data-stu-id="e690f-113">_ppfcnt_</span></span>
  
> <span data-ttu-id="e690f-114">[out] Puntero a un puntero a la interfaz de la biblioteca de formularios local.</span><span class="sxs-lookup"><span data-stu-id="e690f-114">[out] Pointer to a pointer to the local form library interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e690f-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e690f-115">Return value</span></span>

<span data-ttu-id="e690f-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e690f-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e690f-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e690f-117">Remarks</span></span>

<span data-ttu-id="e690f-118">La interfaz a la que se devuelve un puntero se puede usar los programas de instalación de terceros para instalar formularios específicos de la aplicación en la biblioteca sin el programa primero iniciar sesión en MAPI.</span><span class="sxs-lookup"><span data-stu-id="e690f-118">The interface to which a pointer is returned can be used by third-party installation programs to install application-specific forms into the library without the program first having to log on to MAPI.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e690f-119">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e690f-119">MFCMAPI reference</span></span>

<span data-ttu-id="e690f-120">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="e690f-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e690f-121">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="e690f-121">**File**</span></span>|<span data-ttu-id="e690f-122">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="e690f-122">**Function**</span></span>|<span data-ttu-id="e690f-123">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="e690f-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e690f-124">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="e690f-124">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="e690f-125">CMainDlg::OnMAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="e690f-125">CMainDlg::OnMAPIOpenLocalFormContainer</span></span>  <br/> |<span data-ttu-id="e690f-126">MFCMAPI utiliza el método **MAPIOpenLocalFormContainer** para abrir el contenedor de formulario local para representar en una nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="e690f-126">MFCMAPI uses the **MAPIOpenLocalFormContainer** method to open the local form container to render in a new window.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e690f-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="e690f-127">See also</span></span>



[<span data-ttu-id="e690f-128">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="e690f-128">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

