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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 24461099877af683109c8627eacd22a657d6e156
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430570"
---
# <a name="imapimessagesitegetfolder"></a><span data-ttu-id="83c9b-103">IMAPIMessageSite::GetFolder</span><span class="sxs-lookup"><span data-stu-id="83c9b-103">IMAPIMessageSite::GetFolder</span></span>

  
  
<span data-ttu-id="83c9b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="83c9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="83c9b-105">Devuelve la carpeta en la que se creó o abrió el mensaje actual, si existe dicha carpeta.</span><span class="sxs-lookup"><span data-stu-id="83c9b-105">Returns the folder in which the current message was created or opened, if such a folder exists.</span></span> <span data-ttu-id="83c9b-106">Este método devuelve NULL en el  _parámetro ppFolder_ para los mensajes incrustados, que no se almacenan directamente en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="83c9b-106">This method returns NULL in the  _ppFolder_ parameter for embedded messages, which are not stored directly in a folder.</span></span> 
  
```cpp
HRESULT GetFolder(
  LPMAPIFOLDER FAR * ppFolder
);
```

## <a name="parameters"></a><span data-ttu-id="83c9b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="83c9b-107">Parameters</span></span>

 <span data-ttu-id="83c9b-108">_ppFolder_</span><span class="sxs-lookup"><span data-stu-id="83c9b-108">_ppFolder_</span></span>
  
> <span data-ttu-id="83c9b-109">[salida] Puntero a un puntero a la carpeta devuelta.</span><span class="sxs-lookup"><span data-stu-id="83c9b-109">[out] A pointer to a pointer to the returned folder.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="83c9b-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="83c9b-110">Return value</span></span>

<span data-ttu-id="83c9b-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="83c9b-111">S_OK</span></span> 
  
> <span data-ttu-id="83c9b-112">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="83c9b-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="83c9b-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="83c9b-113">S_FALSE</span></span> 
  
> <span data-ttu-id="83c9b-114">No existe ninguna carpeta para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="83c9b-114">No folder exists for the message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="83c9b-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="83c9b-115">Remarks</span></span>

<span data-ttu-id="83c9b-116">Para obtener una lista de interfaces relacionadas con los servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="83c9b-116">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="83c9b-117">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="83c9b-117">MFCMAPI reference</span></span>

<span data-ttu-id="83c9b-118">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="83c9b-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="83c9b-119">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="83c9b-119">**File**</span></span>|<span data-ttu-id="83c9b-120">**Función**</span><span class="sxs-lookup"><span data-stu-id="83c9b-120">**Function**</span></span>|<span data-ttu-id="83c9b-121">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="83c9b-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="83c9b-122">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="83c9b-122">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="83c9b-123">CMyMAPIFormViewer::GetFolder</span><span class="sxs-lookup"><span data-stu-id="83c9b-123">CMyMAPIFormViewer::GetFolder</span></span>  <br/> |<span data-ttu-id="83c9b-124">MFCMAPI usa el **método IMAPIMessageSite::GetFolder** para devolver el puntero almacenado actualmente en caché a la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="83c9b-124">MFCMAPI uses the **IMAPIMessageSite::GetFolder** method to return the currently cached pointer to the specified folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="83c9b-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="83c9b-125">See also</span></span>



[<span data-ttu-id="83c9b-126">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="83c9b-126">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="83c9b-127">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="83c9b-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="83c9b-128">Interfaces de formulario MAPI</span><span class="sxs-lookup"><span data-stu-id="83c9b-128">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

