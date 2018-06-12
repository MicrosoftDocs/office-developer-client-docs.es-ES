---
title: IMAPIMessageSiteGetFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetFolder
api_type:
- COM
ms.assetid: 9f4b4147-ed98-47cb-a799-ddf028f8e826
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: ea95ea4efbbf50e5551a27eb81fe5d5ab3b73948
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817333"
---
# <a name="imapimessagesitegetfolder"></a><span data-ttu-id="ce11a-103">IMAPIMessageSite::GetFolder</span><span class="sxs-lookup"><span data-stu-id="ce11a-103">IMAPIMessageSite::GetFolder</span></span>

  
  
<span data-ttu-id="ce11a-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ce11a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ce11a-105">Devuelve la carpeta en la que el mensaje actual se ha creado o abierto, si existe una carpeta de este tipo.</span><span class="sxs-lookup"><span data-stu-id="ce11a-105">Returns the folder in which the current message was created or opened, if such a folder exists.</span></span> <span data-ttu-id="ce11a-106">Este método devuelve NULL en el parámetro _ppFolder_ para mensajes incrustados, que no se almacenan directamente en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="ce11a-106">This method returns NULL in the  _ppFolder_ parameter for embedded messages, which are not stored directly in a folder.</span></span> 
  
```cpp
HRESULT GetFolder(
  LPMAPIFOLDER FAR * ppFolder
);
```

## <a name="parameters"></a><span data-ttu-id="ce11a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ce11a-107">Parameters</span></span>

 <span data-ttu-id="ce11a-108">_ppFolder_</span><span class="sxs-lookup"><span data-stu-id="ce11a-108">_ppFolder_</span></span>
  
> <span data-ttu-id="ce11a-109">[out] Un puntero a un puntero a la carpeta devuelto.</span><span class="sxs-lookup"><span data-stu-id="ce11a-109">[out] A pointer to a pointer to the returned folder.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ce11a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce11a-110">Return value</span></span>

<span data-ttu-id="ce11a-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="ce11a-111">S_OK</span></span> 
  
> <span data-ttu-id="ce11a-112">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="ce11a-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="ce11a-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="ce11a-113">S_FALSE</span></span> 
  
> <span data-ttu-id="ce11a-114">No existe ninguna carpeta para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="ce11a-114">No folder exists for the message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ce11a-115">Notas</span><span class="sxs-lookup"><span data-stu-id="ce11a-115">Remarks</span></span>

<span data-ttu-id="ce11a-116">Para obtener una lista de las interfaces que están relacionadas con los servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="ce11a-116">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ce11a-117">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ce11a-117">MFCMAPI reference</span></span>

<span data-ttu-id="ce11a-118">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="ce11a-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ce11a-119">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="ce11a-119">**File**</span></span>|<span data-ttu-id="ce11a-120">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="ce11a-120">**Function**</span></span>|<span data-ttu-id="ce11a-121">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="ce11a-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ce11a-122">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="ce11a-122">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="ce11a-123">CMyMAPIFormViewer::GetFolder</span><span class="sxs-lookup"><span data-stu-id="ce11a-123">CMyMAPIFormViewer::GetFolder</span></span>  <br/> |<span data-ttu-id="ce11a-124">MFCMAPI usa el método **IMAPIMessageSite::GetFolder** para devolver el puntero actualmente en caché para la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="ce11a-124">MFCMAPI uses the **IMAPIMessageSite::GetFolder** method to return the currently cached pointer to the specified folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ce11a-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="ce11a-125">See also</span></span>



[<span data-ttu-id="ce11a-126">IMAPIMessageSite: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ce11a-126">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="ce11a-127">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="ce11a-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="ce11a-128">Interfaces de formulario MAPI</span><span class="sxs-lookup"><span data-stu-id="ce11a-128">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

