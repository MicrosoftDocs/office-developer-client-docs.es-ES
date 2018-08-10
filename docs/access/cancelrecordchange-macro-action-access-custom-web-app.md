---
title: Acción de Macro CancelarCambioDeRegistro (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: cbdbee8c-70d6-45df-a56b-5f7c6e5bdc6d
description: Puede utilizar la acción CancelarCambioDeRegistro para cancelar los cambios aplicados a un registro en un bloque de datos CrearRegistro o EditarRegistro antes de que se confirmen los cambios.
ms.openlocfilehash: 5f5d131ce8662dbd290a30ea08594cb413791d5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815341"
---
# <a name="cancelrecordchange-macro-action-access-custom-web-app"></a><span data-ttu-id="817f1-103">Acción de Macro CancelarCambioDeRegistro (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="817f1-103">CancelRecordChange Macro Action (Access custom web app)</span></span>

<span data-ttu-id="817f1-104">Puede utilizar la acción **CancelarCambioDeRegistro** para cancelar los cambios aplicados a un registro en un bloque de datos **[CrearRegistro](createrecord-data-block-access-custom-web-app.md)** o **[EditarRegistro](editrecord-data-block-access-custom-web-app.md)** antes de que se confirmen los cambios.</span><span class="sxs-lookup"><span data-stu-id="817f1-104">You can use the **CancelRecordChange** action to cancel the changes applied to a record in a **[CreateRecord](createrecord-data-block-access-custom-web-app.md)** or **[EditRecord](editrecord-data-block-access-custom-web-app.md)** data block before the changes are committed.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="817f1-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="817f1-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="817f1-107">[!NOTA] La acción **CancelarCambioDeRegistro** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="817f1-107">The **CancelRecordChange** action is available only in Data Macros.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="817f1-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="817f1-108">Remarks</span></span>

<span data-ttu-id="817f1-109">Cuando se llama a la acción **CancelarCambioDeRegistro**, se sale inmediatamente del bloque de datos **CrearRegistro** o **EditarRegistro**.</span><span class="sxs-lookup"><span data-stu-id="817f1-109">When you call the **CancelRecordChange** action, the **CreateRecord** or **EditRecord** data block is exited immediately.</span></span> 
  
