---
title: EliminarRegistro (acción de macro de datos) (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: f6b68a9a-e04a-476e-a407-b1779fea1953
description: Puede usar la acción EliminarRegistro para eliminar un registro.
ms.openlocfilehash: 0e8a658b944e894e4d4014fb3d3d9a583efbee8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423156"
---
# <a name="deleterecord-data-macro-action-access-custom-web-app"></a><span data-ttu-id="d217e-103">EliminarRegistro (acción de macro) (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="d217e-103">DeleteRecord Data Macro action (Access custom web app)</span></span>

<span data-ttu-id="d217e-104">Puede usar la acción **EliminarRegistro** para eliminar un registro.</span><span class="sxs-lookup"><span data-stu-id="d217e-104">You can use the **DeleteRecord** action to delete a record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="d217e-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="d217e-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="d217e-107">Configuración</span><span class="sxs-lookup"><span data-stu-id="d217e-107">Setting</span></span>

<span data-ttu-id="d217e-108">La **acción EliminarRegistro** tiene los argumentos siguientes.</span><span class="sxs-lookup"><span data-stu-id="d217e-108">The **DeleteRecord** action has the following arguments.</span></span> 
  
|<span data-ttu-id="d217e-109">**Argumento**</span><span class="sxs-lookup"><span data-stu-id="d217e-109">**Argument**</span></span>|<span data-ttu-id="d217e-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d217e-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d217e-111">**Alias del registro**</span><span class="sxs-lookup"><span data-stu-id="d217e-111">**Record Alias**</span></span> <br/> |<span data-ttu-id="d217e-112">Una cadena que identifica el registro que hay que eliminar.</span><span class="sxs-lookup"><span data-stu-id="d217e-112">A string that identifies the record to delete.</span></span> <span data-ttu-id="d217e-113">Si no  *se especifica*  el argumento Alias, se elimina el registro actual.</span><span class="sxs-lookup"><span data-stu-id="d217e-113">If the  *Alias*  argument is not specified, then the current record is deleted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d217e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d217e-114">Remarks</span></span>

<span data-ttu-id="d217e-115">Puede utilizar la variable local **ÚltimaIdentidadDeRegistroCreada** para trabajar con el último registro creado en un bloque de datos **CrearRegistro**.</span><span class="sxs-lookup"><span data-stu-id="d217e-115">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="d217e-116">Por ejemplo, use la siguiente sintaxis para hacer referencia al registro creado más recientemente:</span><span class="sxs-lookup"><span data-stu-id="d217e-116">For example, use the following syntax to refer to the most recently created record:</span></span> 
  
`[LastCreateRecordIdentity]`


