---
title: Bloque de datos EditarRegistro (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 54975434-78b2-4010-b2f9-f277831fa92e
description: Puede utilizar el bloque de datos EditarRegistro para cambiar los valores contenidos en un registro existente.
ms.openlocfilehash: 6c214e48326a93cff220b5436d7e7802cd6e3431
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815319"
---
# <a name="editrecord-data-block-access-custom-web-app"></a><span data-ttu-id="735c3-103">Bloque de datos EditarRegistro (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="735c3-103">EditRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="735c3-104">Puede utilizar el bloque de datos **EditarRegistro** para cambiar los valores contenidos en un registro existente.</span><span class="sxs-lookup"><span data-stu-id="735c3-104">You can use the **EditRecord** data block to change the values contained in an existing record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="735c3-p101">[!IMPORTANTE] Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="735c3-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="735c3-107">[!NOTA] El bloque de datos **EditarRegistro** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="735c3-107">The **EditRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="735c3-108">Valores</span><span class="sxs-lookup"><span data-stu-id="735c3-108">Setting</span></span>

<span data-ttu-id="735c3-109">El bloque de datos **EditarRegistro** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="735c3-109">The **EditRecord** data block has the following arguments.</span></span> 
  
|<span data-ttu-id="735c3-110">**Argumento**</span><span class="sxs-lookup"><span data-stu-id="735c3-110">**Argument**</span></span>|<span data-ttu-id="735c3-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="735c3-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="735c3-112">**Alias**</span><span class="sxs-lookup"><span data-stu-id="735c3-112">**Alias**</span></span> <br/> |<span data-ttu-id="735c3-113">Una cadena que identifica el registro para editar.</span><span class="sxs-lookup"><span data-stu-id="735c3-113">A string that identifies the record to edit.</span></span> <span data-ttu-id="735c3-114">Si no se especifica el argumento de *Alias* , a continuación, se edita el registro actual.</span><span class="sxs-lookup"><span data-stu-id="735c3-114">If the  *Alias*  argument is not specified, then the current record is edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="735c3-115">Notas</span><span class="sxs-lookup"><span data-stu-id="735c3-115">Remarks</span></span>

<span data-ttu-id="735c3-116">Después de la instrucción **EditarRegistro** , puede insertar un bloque de comandos que se ejecutará antes de que se confirman los cambios realizados en el registro.</span><span class="sxs-lookup"><span data-stu-id="735c3-116">After the **EditRecord** statement, you can insert a block of commands that will execute before the changes to the record are committed.</span></span> <span data-ttu-id="735c3-117">Las siguientes acciones están disponibles en un bloque de datos **EditarRegistro** .</span><span class="sxs-lookup"><span data-stu-id="735c3-117">The following actions are available in an **EditRecord** data block.</span></span> 
  
||
|:-----|
|[<span data-ttu-id="735c3-118">CancelarCambioDeRegistro (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="735c3-118">CancelRecordChange Macro Action</span></span>](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="735c3-119">Comentario (instrucción de macro)</span><span class="sxs-lookup"><span data-stu-id="735c3-119">Comment Macro Statement</span></span>](comment-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="735c3-120">Grupo (instrucción de macro)</span><span class="sxs-lookup"><span data-stu-id="735c3-120">Group Macro Statement</span></span>](group-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="735c3-121">If... A continuación... Instrucción de Macro Else</span><span class="sxs-lookup"><span data-stu-id="735c3-121">If...Then...Else Macro Statement</span></span>](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="735c3-122">EstablecerCampo (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="735c3-122">SetField Macro Action</span></span>](setfield-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="735c3-123">EstablecerVariableLocal (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="735c3-123">SetLocalVar Macro Action</span></span>](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
<span data-ttu-id="735c3-124">Utilice la acción de **EstablecerCampo** para especificar los nuevos valores de un campo en el registro editado.</span><span class="sxs-lookup"><span data-stu-id="735c3-124">Use the **SetField** action to specify the new values of a field in the edited record.</span></span> 
  
<span data-ttu-id="735c3-125">Puede usar un **Si... A continuación... Else** instrucción para realizar operaciones en función de una condición.</span><span class="sxs-lookup"><span data-stu-id="735c3-125">You can use an **If...Then...Else** statement to perform operations based on a condition.</span></span> 
  
<span data-ttu-id="735c3-p104">Para cancelar la edición de un registro, utilice la acción **CancelarCambioDeRegistro**. Esto evita que se confirmen los cambios y permite salir del bloque de datos **EditarRegistro**.</span><span class="sxs-lookup"><span data-stu-id="735c3-p104">To cancel the editing of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **EditRecord** data block.</span></span> 
  
<span data-ttu-id="735c3-128">Puede utilizar la variable local **ÚltimaIdentidadDeRegistroCreada** para trabajar con el último registro creado en un bloque de datos **CrearRegistro**.</span><span class="sxs-lookup"><span data-stu-id="735c3-128">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="735c3-129">Por ejemplo, utilice la siguiente sintaxis para hacer referencia al campo AssignedTo del registro creado más recientemente:</span><span class="sxs-lookup"><span data-stu-id="735c3-129">For example, use the following syntax to refer to the AssignedTo field of the most recently created record:</span></span> 
  
`[LastCreateRecordIdentity].[AssignedTo]`


