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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ace31079c51aac169f6091af0cb363e7f05f0d14
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270150"
---
# <a name="mapiopenlocalformcontainer"></a><span data-ttu-id="24a61-103">MAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="24a61-103">MAPIOpenLocalFormContainer</span></span>

  
  
<span data-ttu-id="24a61-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24a61-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24a61-105">Devuelve un puntero de interfaz a la biblioteca de formularios local.</span><span class="sxs-lookup"><span data-stu-id="24a61-105">Returns an interface pointer to the local form library.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="24a61-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="24a61-106">Header file:</span></span>  <br/> |<span data-ttu-id="24a61-107">MAPIForm. h</span><span class="sxs-lookup"><span data-stu-id="24a61-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="24a61-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="24a61-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="24a61-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="24a61-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="24a61-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="24a61-110">Called by:</span></span>  <br/> |<span data-ttu-id="24a61-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="24a61-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenLocalFormContainer(
  LPMAPIFORMCONTAINER FAR * ppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="24a61-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="24a61-112">Parameters</span></span>

 <span data-ttu-id="24a61-113">_ppfcnt_</span><span class="sxs-lookup"><span data-stu-id="24a61-113">_ppfcnt_</span></span>
  
> <span data-ttu-id="24a61-114">contempla Puntero a un puntero a la interfaz de la biblioteca de formularios local.</span><span class="sxs-lookup"><span data-stu-id="24a61-114">[out] Pointer to a pointer to the local form library interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="24a61-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="24a61-115">Return value</span></span>

<span data-ttu-id="24a61-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="24a61-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="24a61-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="24a61-117">Remarks</span></span>

<span data-ttu-id="24a61-118">Los programas de instalación de terceros pueden usar la interfaz en la que se devuelve un puntero para instalar formularios específicos de la aplicación en la biblioteca sin que el programa tenga que iniciar sesión en MAPI.</span><span class="sxs-lookup"><span data-stu-id="24a61-118">The interface to which a pointer is returned can be used by third-party installation programs to install application-specific forms into the library without the program first having to log on to MAPI.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="24a61-119">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="24a61-119">MFCMAPI reference</span></span>

<span data-ttu-id="24a61-120">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="24a61-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="24a61-121">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="24a61-121">**File**</span></span>|<span data-ttu-id="24a61-122">**Función**</span><span class="sxs-lookup"><span data-stu-id="24a61-122">**Function**</span></span>|<span data-ttu-id="24a61-123">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="24a61-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="24a61-124">MainDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="24a61-124">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="24a61-125">CMainDlg:: OnMAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="24a61-125">CMainDlg::OnMAPIOpenLocalFormContainer</span></span>  <br/> |<span data-ttu-id="24a61-126">MFCMAPI usa el método **MAPIOpenLocalFormContainer** para abrir el contenedor de formulario local para representarlo en una ventana nueva.</span><span class="sxs-lookup"><span data-stu-id="24a61-126">MFCMAPI uses the **MAPIOpenLocalFormContainer** method to open the local form container to render in a new window.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="24a61-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="24a61-127">See also</span></span>



[<span data-ttu-id="24a61-128">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="24a61-128">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

