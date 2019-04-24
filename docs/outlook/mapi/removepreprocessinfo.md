---
title: RemovePreprocessInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.RemovePreprocessInfo
api_type:
- COM
ms.assetid: 25f46937-abac-4a0b-83db-eeac9451c112
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d80c73aef780a0da39f3939f71462488a067de5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328381"
---
# <a name="removepreprocessinfo"></a><span data-ttu-id="78246-103">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="78246-103">RemovePreprocessInfo</span></span>

  
  
<span data-ttu-id="78246-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78246-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78246-105">Quita la información preprocesada escrita por una función basada en [PreprocessMessage](preprocessmessage.md) de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="78246-105">Removes preprocessed information written by a [PreprocessMessage](preprocessmessage.md) based function from a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="78246-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="78246-106">Header file:</span></span>  <br/> |<span data-ttu-id="78246-107">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="78246-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="78246-108">Función definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="78246-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="78246-109">Proveedores de transporte</span><span class="sxs-lookup"><span data-stu-id="78246-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="78246-110">Función definida llamada por:</span><span class="sxs-lookup"><span data-stu-id="78246-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="78246-111">Cola MAPI</span><span class="sxs-lookup"><span data-stu-id="78246-111">MAPI spooler</span></span>  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a><span data-ttu-id="78246-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="78246-112">Parameters</span></span>

 <span data-ttu-id="78246-113">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="78246-113">_lpMessage_</span></span>
  
> <span data-ttu-id="78246-114">a Puntero al mensaje preprocesado desde el que se va a quitar la información.</span><span class="sxs-lookup"><span data-stu-id="78246-114">[in] Pointer to the preprocessed message from which information is to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="78246-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="78246-115">Return value</span></span>

<span data-ttu-id="78246-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="78246-116">S_OK</span></span>
  
> <span data-ttu-id="78246-117">La información preprocesada se quitó correctamente.</span><span class="sxs-lookup"><span data-stu-id="78246-117">Preprocessed information was removed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="78246-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="78246-118">Remarks</span></span>

<span data-ttu-id="78246-119">La cola MAPI llama a una función basada en **RemovePreprocessInfo**.</span><span class="sxs-lookup"><span data-stu-id="78246-119">The MAPI spooler calls a function based on **RemovePreprocessInfo**.</span></span> <span data-ttu-id="78246-120">Un proveedor de transporte registra la función basada en **RemovePreprocessInfo** a la vez que registra la función Parallel **PreprocessMessage** basada en una llamada al método [IMAPISupport:: RegisterPreprocessor](imapisupport-registerpreprocessor.md) .</span><span class="sxs-lookup"><span data-stu-id="78246-120">A transport provider registers the **RemovePreprocessInfo** based function at the same time it registers the parallel **PreprocessMessage** based function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> 
  
<span data-ttu-id="78246-121">Una representación de imágenes adecuada para la transmisión de fax es un ejemplo de información preprocesada escrita por una función definida por el prototipo de función [PreprocessMessage](preprocessmessage.md).</span><span class="sxs-lookup"><span data-stu-id="78246-121">An image rendering suitable for fax transmission is an example of preprocessed information written by a function defined by the [PreprocessMessage](preprocessmessage.md)function prototype.</span></span> <span data-ttu-id="78246-122">La cola MAPI suele llamar a una función **RemovePreprocessInfo** después de enviar un mensaje que contiene información preprocesada.</span><span class="sxs-lookup"><span data-stu-id="78246-122">The MAPI spooler usually calls a **RemovePreprocessInfo** function after sending a message that contains preprocessed information.</span></span> 
  

