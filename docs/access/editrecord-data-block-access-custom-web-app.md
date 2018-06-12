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
# <a name="editrecord-data-block-access-custom-web-app"></a>Bloque de datos EditarRegistro (aplicación web personalizado de Access)

Puede utilizar el bloque de datos **EditarRegistro** para cambiar los valores contenidos en un registro existente. 
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
> [!NOTE]
> [!NOTA] El bloque de datos **EditarRegistro** solo está disponible en macros de datos. 
  
## <a name="setting"></a>Valores

El bloque de datos **EditarRegistro** tiene los siguientes argumentos. 
  
|**Argumento**|**Descripción**|
|:-----|:-----|
|**Alias** <br/> |Una cadena que identifica el registro para editar. Si no se especifica el argumento de *Alias* , a continuación, se edita el registro actual.  <br/> |
   
## <a name="remarks"></a>Notas

Después de la instrucción **EditarRegistro** , puede insertar un bloque de comandos que se ejecutará antes de que se confirman los cambios realizados en el registro. Las siguientes acciones están disponibles en un bloque de datos **EditarRegistro** . 
  
||
|:-----|
|[CancelarCambioDeRegistro (acción de macro)](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[Comentario (instrucción de macro)](comment-macro-block-access-custom-web-app.md) <br/> |
|[Grupo (instrucción de macro)](group-macro-block-access-custom-web-app.md) <br/> |
|[If... A continuación... Instrucción de Macro Else](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[EstablecerCampo (acción de macro)](setfield-macro-action-access-custom-web-app.md) <br/> |
|[EstablecerVariableLocal (acción de macro)](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
Utilice la acción de **EstablecerCampo** para especificar los nuevos valores de un campo en el registro editado. 
  
Puede usar un **Si... A continuación... Else** instrucción para realizar operaciones en función de una condición. 
  
Para cancelar la edición de un registro, utilice la acción **CancelarCambioDeRegistro**. Esto evita que se confirmen los cambios y permite salir del bloque de datos **EditarRegistro**. 
  
Puede utilizar la variable local **ÚltimaIdentidadDeRegistroCreada** para trabajar con el último registro creado en un bloque de datos **CrearRegistro**. Por ejemplo, utilice la siguiente sintaxis para hacer referencia al campo AssignedTo del registro creado más recientemente: 
  
`[LastCreateRecordIdentity].[AssignedTo]`


