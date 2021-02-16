---
title: Acción de macro SetField (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 9ae292b0-fde0-4c2b-ba23-23e90365597d
description: La acción EstablecerCampo puede utilizarse para asignar un valor a un campo.
ms.openlocfilehash: c67c66c238b68512aec90cf6d82d7d497e16ecf1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432929"
---
# <a name="setfield-macro-action-access-custom-web-app"></a><span data-ttu-id="dd6e7-103">Acción de macro SetField (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="dd6e7-103">SetField Macro Action (Access custom web app)</span></span>

<span data-ttu-id="dd6e7-104">La acción **EstablecerCampo** puede utilizarse para asignar un valor a un campo.</span><span class="sxs-lookup"><span data-stu-id="dd6e7-104">The **SetField** action can be used to assign a value to a field.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="dd6e7-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="dd6e7-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="dd6e7-107">La acción **EstablecerCampo** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="dd6e7-107">The **SetField** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="dd6e7-108">Setting</span><span class="sxs-lookup"><span data-stu-id="dd6e7-108">Setting</span></span>

<span data-ttu-id="dd6e7-109">La acción **EstablecerCampo** utiliza los argumentos enumerados en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="dd6e7-109">The **SetField** action has the arguments listed in the following table.</span></span> 
  
|<span data-ttu-id="dd6e7-110">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="dd6e7-110">**Argument name**</span></span>|<span data-ttu-id="dd6e7-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dd6e7-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dd6e7-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="dd6e7-112">**Name**</span></span> <br/> |<span data-ttu-id="dd6e7-113">Una cadena que identifica el campo.</span><span class="sxs-lookup"><span data-stu-id="dd6e7-113">A string that identifies the field.</span></span>  <br/> |
|<span data-ttu-id="dd6e7-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="dd6e7-114">**Value**</span></span> <br/> |<span data-ttu-id="dd6e7-115">Expresión que especifica el valor que se asignará al campo.</span><span class="sxs-lookup"><span data-stu-id="dd6e7-115">An expression that specifies the value to assign to the field.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd6e7-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dd6e7-116">Remarks</span></span>

<span data-ttu-id="dd6e7-117">La **acción SetField** no se puede usar fuera de un bloque de datos **[CreateRecord](createrecord-data-block-access-custom-web-app.md)** o **[EditRecord.](editrecord-data-block-access-custom-web-app.md)**</span><span class="sxs-lookup"><span data-stu-id="dd6e7-117">The **SetField** action cannot be used outside of a **[CreateRecord](createrecord-data-block-access-custom-web-app.md)** or **[EditRecord](editrecord-data-block-access-custom-web-app.md)** data block.</span></span> 
  

