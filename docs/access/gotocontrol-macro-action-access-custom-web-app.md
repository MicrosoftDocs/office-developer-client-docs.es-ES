---
title: Acción de macro GoToControl (aplicación web de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 6c286821-67d6-4d96-973a-bca7934c7672
description: Puede usar la acción GoToControl para mover el foco al control especificado en el registro actual de la vista abierta.
ms.openlocfilehash: 2368933a6277615554a565d3bdd973f7d1f366f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436478"
---
# <a name="gotocontrol-macro-action-access-custom-web-app"></a><span data-ttu-id="57a48-103">Acción de macro GoToControl (aplicación web de Access)</span><span class="sxs-lookup"><span data-stu-id="57a48-103">GoToControl Macro Action (Access custom web app)</span></span>

<span data-ttu-id="57a48-104">Puede usar la acción **GoToControl** para mover el foco al control especificado en el registro actual de la vista abierta.</span><span class="sxs-lookup"><span data-stu-id="57a48-104">You can use the **GoToControl** action to move the focus to the specified control in the current record of the open view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="57a48-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="57a48-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="57a48-107">Configuración</span><span class="sxs-lookup"><span data-stu-id="57a48-107">Setting</span></span>

<span data-ttu-id="57a48-108">La acción **GoToControl** tiene el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="57a48-108">The **GoToControl** action has the following argument.</span></span> 
  
|<span data-ttu-id="57a48-109">**Argumento de la acción**</span><span class="sxs-lookup"><span data-stu-id="57a48-109">**Action argument**</span></span>|<span data-ttu-id="57a48-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="57a48-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="57a48-111">**Nombre del control**</span><span class="sxs-lookup"><span data-stu-id="57a48-111">**Control Name**</span></span> <br/> |<span data-ttu-id="57a48-112">El nombre del campo o control donde desea el foco.</span><span class="sxs-lookup"><span data-stu-id="57a48-112">The name of the field or control where you want the focus.</span></span> <span data-ttu-id="57a48-113">Este argumento es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="57a48-113">This is a required argument.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="57a48-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="57a48-114">Remarks</span></span>

<span data-ttu-id="57a48-115">Puede usar esta acción si desea que un campo o control concreto tenga el foco.</span><span class="sxs-lookup"><span data-stu-id="57a48-115">You can use this action when you want a particular field or control to have the focus.</span></span> <span data-ttu-id="57a48-116">También puede usar esta acción para desplazarse por un formulario según ciertas condiciones.</span><span class="sxs-lookup"><span data-stu-id="57a48-116">You can also use this action to navigate in a form according to certain conditions.</span></span> <span data-ttu-id="57a48-117">Por ejemplo, si el usuario escribe No en un control Casado en un formulario de seguros de salud, el foco puede omitir automáticamente el control Nombre de cónyuge y pasar al siguiente control.</span><span class="sxs-lookup"><span data-stu-id="57a48-117">For example, if the user enters No in a Married control on a health insurance form, the focus can automatically skip the Spouse/partner Name control and move to the next control.</span></span>
  

