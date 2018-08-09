---
title: Acción de Macro Provocarerror (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5e29bf64-300a-4094-82ff-664e79782d86
description: La acción Provocarerror muestra una ventana emergente que contiene un mensaje de error especificado.
ms.openlocfilehash: 1176804106c5cfd9d4bd30f79f47975593089dbc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815475"
---
# <a name="raiseerror-macro-action-access-custom-web-app"></a><span data-ttu-id="d4bcc-103">Acción de Macro Provocarerror (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="d4bcc-103">RaiseError Macro Action (Access custom web app)</span></span>

<span data-ttu-id="d4bcc-104">La acción **Provocarerror** muestra una ventana emergente que contiene un mensaje de error especificado.</span><span class="sxs-lookup"><span data-stu-id="d4bcc-104">The **RaiseError** action displays a popup window that contains a specified error message.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="d4bcc-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="d4bcc-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d4bcc-107">[!NOTA] La acción **ProvocarError** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="d4bcc-107">The **RaiseError** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="d4bcc-108">Valores</span><span class="sxs-lookup"><span data-stu-id="d4bcc-108">Setting</span></span>

<span data-ttu-id="d4bcc-109">La acción **Provocarerror** tiene el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="d4bcc-109">The **RaiseError** action has the following argument.</span></span> 
  
|<span data-ttu-id="d4bcc-110">**Argumento**</span><span class="sxs-lookup"><span data-stu-id="d4bcc-110">**Argument**</span></span>|<span data-ttu-id="d4bcc-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d4bcc-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d4bcc-112">_Descripción del error_</span><span class="sxs-lookup"><span data-stu-id="d4bcc-112">_Error Description_</span></span> <br/> |<span data-ttu-id="d4bcc-113">Una expresión de cadena que describe el error.</span><span class="sxs-lookup"><span data-stu-id="d4bcc-113">A string expression that describes the error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4bcc-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d4bcc-114">Remarks</span></span>

<span data-ttu-id="d4bcc-115">Cuando se llama a la acción **Provocarerror** , todas las operaciones en la transacción actual se deshacen.</span><span class="sxs-lookup"><span data-stu-id="d4bcc-115">When the **RaiseError** action is called, all of the operations in the current transaction are rolled back.</span></span> 
  

