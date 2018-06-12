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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: fab8860621cee5a87b087ee9d98f373baa278e45
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820526"
---
# <a name="removepreprocessinfo"></a><span data-ttu-id="d55af-103">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="d55af-103">RemovePreprocessInfo</span></span>

  
  
<span data-ttu-id="d55af-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d55af-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d55af-105">Quita preprocesa escrita por una función [PreprocessMessage](preprocessmessage.md) en función de un mensaje de información.</span><span class="sxs-lookup"><span data-stu-id="d55af-105">Removes preprocessed information written by a [PreprocessMessage](preprocessmessage.md) based function from a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d55af-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d55af-106">Header file:</span></span>  <br/> |<span data-ttu-id="d55af-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="d55af-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="d55af-108">Función definido implementada por:</span><span class="sxs-lookup"><span data-stu-id="d55af-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="d55af-109">Proveedores de transporte</span><span class="sxs-lookup"><span data-stu-id="d55af-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="d55af-110">Llamado por una función definida:</span><span class="sxs-lookup"><span data-stu-id="d55af-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="d55af-111">Cola MAPI</span><span class="sxs-lookup"><span data-stu-id="d55af-111">MAPI spooler</span></span>  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a><span data-ttu-id="d55af-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d55af-112">Parameters</span></span>

 <span data-ttu-id="d55af-113">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="d55af-113">_lpMessage_</span></span>
  
> <span data-ttu-id="d55af-114">[entrada] Puntero al mensaje preprocesado desde la que es información que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="d55af-114">[in] Pointer to the preprocessed message from which information is to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d55af-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d55af-115">Return value</span></span>

<span data-ttu-id="d55af-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="d55af-116">S_OK</span></span>
  
> <span data-ttu-id="d55af-117">Información preprocesado se quitó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d55af-117">Preprocessed information was removed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d55af-118">Notas</span><span class="sxs-lookup"><span data-stu-id="d55af-118">Remarks</span></span>

<span data-ttu-id="d55af-119">La cola MAPI llama a una función según **RemovePreprocessInfo**.</span><span class="sxs-lookup"><span data-stu-id="d55af-119">The MAPI spooler calls a function based on **RemovePreprocessInfo**.</span></span> <span data-ttu-id="d55af-120">Un proveedor de transporte registra la función **RemovePreprocessInfo** en función al mismo tiempo que registra la función **PreprocessMessage** basado paralela en una llamada al método [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) .</span><span class="sxs-lookup"><span data-stu-id="d55af-120">A transport provider registers the **RemovePreprocessInfo** based function at the same time it registers the parallel **PreprocessMessage** based function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> 
  
<span data-ttu-id="d55af-121">Una imagen de representación adecuada para la transmisión de fax es un ejemplo de información preprocesado escrita por una función definida por el prototipo de función [PreprocessMessage](preprocessmessage.md).</span><span class="sxs-lookup"><span data-stu-id="d55af-121">An image rendering suitable for fax transmission is an example of preprocessed information written by a function defined by the [PreprocessMessage](preprocessmessage.md)function prototype.</span></span> <span data-ttu-id="d55af-122">La cola MAPI normalmente llama a una función de **RemovePreprocessInfo** después de enviar un mensaje que contiene información preprocesado.</span><span class="sxs-lookup"><span data-stu-id="d55af-122">The MAPI spooler usually calls a **RemovePreprocessInfo** function after sending a message that contains preprocessed information.</span></span> 
  

