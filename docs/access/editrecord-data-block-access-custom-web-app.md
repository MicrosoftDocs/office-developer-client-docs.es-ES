---
title: Bloque de datos EditRecord (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 54975434-78b2-4010-b2f9-f277831fa92e
description: Puede utilizar el bloque de datos EditarRegistro para cambiar los valores contenidos en un registro existente.
ms.openlocfilehash: 0d9ef6c7689b44a0304309a7537e744eff97c809
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418347"
---
# <a name="editrecord-data-block-access-custom-web-app"></a>Bloque de datos EditRecord (aplicación web personalizada de Access)

Puede utilizar el bloque de datos **EditarRegistro** para cambiar los valores contenidos en un registro existente. 
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
> [!NOTE]
> El bloque de datos **EditarRegistro** solo está disponible en macros de datos. 
  
## <a name="setting"></a>Setting

El bloque de datos **EditarRegistro** tiene los siguientes argumentos. 
  
|**Argumento**|**Descripción**|
|:-----|:-----|
|**Alias** <br/> |Una cadena que identifica el registro que hay que editar. Si no  *se especifica*  el argumento Alias, se edita el registro actual.  <br/> |
   
## <a name="remarks"></a>Comentarios

Después de **la instrucción EditRecord,** puede insertar un bloque de comandos que se ejecutará antes de que se confirman los cambios realizados en el registro. Las siguientes acciones están disponibles en un **bloque de datos EditRecord.** 
  
||
|:-----|
|[CancelarCambioDeRegistro (acción de macro)](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[Comentario (instrucción de macro)](comment-macro-block-access-custom-web-app.md) <br/> |
|[Grupo (instrucción de macro)](group-macro-block-access-custom-web-app.md) <br/> |
|[Si...Entonces...Sino (instrucción de macro)](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[EstablecerCampo (acción de macro)](setfield-macro-action-access-custom-web-app.md) <br/> |
|[EstablecerVariableLocal (acción de macro)](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
Utilice la acción de **EstablecerCampo** para especificar los nuevos valores de un campo en el registro editado. 
  
Puede usar un **if... A continuación... Instrucción Else** para realizar operaciones basadas en una condición. 
  
Para cancelar la edición de un registro, utilice la acción **CancelarCambioDeRegistro**. Esto evita que se confirmen los cambios y permite salir del bloque de datos **EditarRegistro**. 
  
Puede utilizar la variable local **ÚltimaIdentidadDeRegistroCreada** para trabajar con el último registro creado en un bloque de datos **CrearRegistro**. Por ejemplo, use la siguiente sintaxis para hacer referencia al campo AssignedTo del registro creado más recientemente: 
  
`[LastCreateRecordIdentity].[AssignedTo]`


