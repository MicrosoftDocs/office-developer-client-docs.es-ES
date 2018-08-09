---
title: Acción de Macro SetField (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 9ae292b0-fde0-4c2b-ba23-23e90365597d
description: La acción EstablecerCampo puede utilizarse para asignar un valor a un campo.
ms.openlocfilehash: 1221ea408540a960b948d2d3ece272fd71cb3daf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815492"
---
# <a name="setfield-macro-action-access-custom-web-app"></a><span data-ttu-id="d3f2d-103">Acción de Macro SetField (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="d3f2d-103">SetField Macro Action (Access custom web app)</span></span>

<span data-ttu-id="d3f2d-104">La acción **EstablecerCampo** puede utilizarse para asignar un valor a un campo.</span><span class="sxs-lookup"><span data-stu-id="d3f2d-104">The **SetField** action can be used to assign a value to a field.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="d3f2d-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="d3f2d-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d3f2d-107">[!NOTA] La acción **EstablecerCampo** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="d3f2d-107">The **SetField** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="d3f2d-108">Valores</span><span class="sxs-lookup"><span data-stu-id="d3f2d-108">Setting</span></span>

<span data-ttu-id="d3f2d-109">La acción **EstablecerCampo** utiliza los argumentos enumerados en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="d3f2d-109">The **SetField** action has the arguments listed in the following table.</span></span> 
  
|<span data-ttu-id="d3f2d-110">**Nombre del argumento**</span><span class="sxs-lookup"><span data-stu-id="d3f2d-110">**Argument name**</span></span>|<span data-ttu-id="d3f2d-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d3f2d-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d3f2d-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="d3f2d-112">**Name**</span></span> <br/> |<span data-ttu-id="d3f2d-113">Una cadena que identifica el campo.</span><span class="sxs-lookup"><span data-stu-id="d3f2d-113">A string that identifies the field.</span></span>  <br/> |
|<span data-ttu-id="d3f2d-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d3f2d-114">**Value**</span></span> <br/> |<span data-ttu-id="d3f2d-115">Una expresión que especifica el valor que se asigna al campo.</span><span class="sxs-lookup"><span data-stu-id="d3f2d-115">An expression that specifies the value to assign to the field.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3f2d-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d3f2d-116">Remarks</span></span>

<span data-ttu-id="d3f2d-117">No se puede usar la acción **EstablecerCampo** fuera de un bloque de datos **[CrearRegistro](createrecord-data-block-access-custom-web-app.md)** o **[EditarRegistro](editrecord-data-block-access-custom-web-app.md)** .</span><span class="sxs-lookup"><span data-stu-id="d3f2d-117">The **SetField** action cannot be used outside of a **[CreateRecord](createrecord-data-block-access-custom-web-app.md)** or **[EditRecord](editrecord-data-block-access-custom-web-app.md)** data block.</span></span> 
  

