---
title: Bloque de datos CreateRecord (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dd73bae-a8d5-4d8b-b356-01ac72f7e5d9
description: Puede utilizar el bloque de datos CrearRegistro para crear un nuevo registro en la tabla especificada.
ms.openlocfilehash: d89b62180dbe50a0c7dab862b70062a47558c25a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421378"
---
# <a name="createrecord-data-block-access-custom-web-app"></a><span data-ttu-id="a7a9f-103">Bloque de datos CreateRecord (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="a7a9f-103">CreateRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="a7a9f-104">Puede utilizar el bloque de datos **CrearRegistro** para crear un nuevo registro en la tabla especificada.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-104">You can use the **CreateRecord** data block to create a new record in the specified table.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="a7a9f-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a7a9f-107">El bloque de datos **CrearRegistro** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-107">The **CreateRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="a7a9f-108">Setting</span><span class="sxs-lookup"><span data-stu-id="a7a9f-108">Setting</span></span>

<span data-ttu-id="a7a9f-109">El bloque de datos **CrearRegistro** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-109">The **CreateRecord** data block has the following arguments.</span></span> 
  
<span data-ttu-id="a7a9f-110">El bloque de datos **CrearRegistro** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-110">The **CreateRecord** data block has the following arguments.</span></span> 
  
|<span data-ttu-id="a7a9f-111">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="a7a9f-111">**Argument name**</span></span>|<span data-ttu-id="a7a9f-112">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="a7a9f-112">**Required**</span></span>|<span data-ttu-id="a7a9f-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a7a9f-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a7a9f-114">**Crear un registro en**</span><span class="sxs-lookup"><span data-stu-id="a7a9f-114">**Create a Record In**</span></span> <br/> |<span data-ttu-id="a7a9f-115">Sí</span><span class="sxs-lookup"><span data-stu-id="a7a9f-115">Yes</span></span>  <br/> |<span data-ttu-id="a7a9f-116">Nombre de la tabla en la que se creará el nuevo registro.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-116">The name of the table to create the new record in.</span></span>  <br/> |
|<span data-ttu-id="a7a9f-117">**Alias**</span><span class="sxs-lookup"><span data-stu-id="a7a9f-117">**Alias**</span></span> <br/> |<span data-ttu-id="a7a9f-118">No</span><span class="sxs-lookup"><span data-stu-id="a7a9f-118">No</span></span>  <br/> |<span data-ttu-id="a7a9f-119">Cadena que identifica el registro.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-119">A string that identifies the record.</span></span> <span data-ttu-id="a7a9f-120">Puede utilizar el alias del registro para identificar</span><span class="sxs-lookup"><span data-stu-id="a7a9f-120">You can use the record's alias to identify</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7a9f-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a7a9f-121">Remarks</span></span>

<span data-ttu-id="a7a9f-122">El registro creado por **CrearRegistro** se convierte automáticamente en el registro actual.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-122">The record created by **CreateRecord** automatically becomes the current record.</span></span> 
  
<span data-ttu-id="a7a9f-123">Después **de la instrucción CreateRecord,** puede insertar un bloque de comandos que se ejecutará antes de que se confirma el nuevo registro.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-123">After **CreateRecord** statement, you can insert a block of commands that will execute before the new record is committed.</span></span> <span data-ttu-id="a7a9f-124">Las acciones siguientes están disponibles en un bloque de datos **CrearRegistro**.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-124">The following actions are available in a **CreateRecord** data block.</span></span> 
  
||
|:-----|
|[<span data-ttu-id="a7a9f-125">CancelarCambioDeRegistro (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="a7a9f-125">CancelRecordChange Macro Action</span></span>](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="a7a9f-126">Comentario (instrucción de macro)</span><span class="sxs-lookup"><span data-stu-id="a7a9f-126">Comment Macro Statement</span></span>](comment-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="a7a9f-127">Grupo (instrucción de macro)</span><span class="sxs-lookup"><span data-stu-id="a7a9f-127">Group Macro Statement</span></span>](group-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="a7a9f-128">Si...Entonces...Sino (instrucción de macro)</span><span class="sxs-lookup"><span data-stu-id="a7a9f-128">If...Then...Else Macro Statement</span></span>](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="a7a9f-129">EstablecerCampo (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="a7a9f-129">SetField Macro Action</span></span>](setfield-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="a7a9f-130">EstablecerVariableLocal (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="a7a9f-130">SetLocalVar Macro Action</span></span>](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
<span data-ttu-id="a7a9f-131">Después de que la acción **CrearRegistro** cree un registro, utilice la acción **EstablecerCampo** para especificar un valor de un campo en el nuevo registro.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-131">After the **CreateRecord** action creates a record, use the **SetField** action to specify a value of a field in the new record.</span></span> 
  
<span data-ttu-id="a7a9f-132">Puede usar un **if... A continuación... Instrucción Else** para realizar operaciones basadas en una condición.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-132">You can use an **If...Then...Else** statement to perform operations based on a condition.</span></span> 
  
<span data-ttu-id="a7a9f-p104">Para cancelar la creación de un registro, utilice la acción **CancelarCambioDeRegistro**. Esto evita que se confirmen los cambios y permite salir del bloque de datos **CrearRegistro**.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-p104">To cancel the creation of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **CreateRecord** data block.</span></span> 
  
<span data-ttu-id="a7a9f-135">Una vez que se confirma el nuevo registro, puede utilizar la variable local **ÚltimaIdentidadDeRegistroCreada** para trabajar con el registro.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-135">Once the new record is committed, you can use the **LastCreateRecordIdentity** local variable to work with the record.</span></span> <span data-ttu-id="a7a9f-136">Por ejemplo, use la siguiente sintaxis para hacer referencia al campo AssignedTo del registro creado más recientemente.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-136">For example, use the following syntax to refer to the AssignedTo field of the most recently created record.</span></span> 
  
`[LastCreateRecordIdentity].[AssignedTo]`


