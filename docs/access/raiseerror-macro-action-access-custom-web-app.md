---
title: Acción de macro RaiseError (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5e29bf64-300a-4094-82ff-664e79782d86
description: La acción RaiseError muestra una ventana emergente que contiene un mensaje de error especificado.
ms.openlocfilehash: 49e544d2234759709c19052b5540d42e88070849
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408246"
---
# <a name="raiseerror-macro-action-access-custom-web-app"></a><span data-ttu-id="2a578-103">Acción de macro RaiseError (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="2a578-103">RaiseError Macro Action (Access custom web app)</span></span>

<span data-ttu-id="2a578-104">La **acción RaiseError** muestra una ventana emergente que contiene un mensaje de error especificado.</span><span class="sxs-lookup"><span data-stu-id="2a578-104">The **RaiseError** action displays a popup window that contains a specified error message.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="2a578-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="2a578-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2a578-107">La acción **ProvocarError** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="2a578-107">The **RaiseError** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="2a578-108">Configuración</span><span class="sxs-lookup"><span data-stu-id="2a578-108">Setting</span></span>

<span data-ttu-id="2a578-109">La **acción RaiseError** tiene el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="2a578-109">The **RaiseError** action has the following argument.</span></span> 
  
|<span data-ttu-id="2a578-110">**Argumento**</span><span class="sxs-lookup"><span data-stu-id="2a578-110">**Argument**</span></span>|<span data-ttu-id="2a578-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2a578-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2a578-112">_Descripción del error_</span><span class="sxs-lookup"><span data-stu-id="2a578-112">_Error Description_</span></span> <br/> |<span data-ttu-id="2a578-113">Una expresión de cadena que describe el error.</span><span class="sxs-lookup"><span data-stu-id="2a578-113">A string expression that describes the error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a578-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2a578-114">Remarks</span></span>

<span data-ttu-id="2a578-115">Cuando se llama a la acción **RaiseError,** se revierte todas las operaciones de la transacción actual.</span><span class="sxs-lookup"><span data-stu-id="2a578-115">When the **RaiseError** action is called, all of the operations in the current transaction are rolled back.</span></span> 
  

