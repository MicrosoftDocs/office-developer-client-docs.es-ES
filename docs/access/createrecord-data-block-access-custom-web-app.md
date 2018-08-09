---
title: Bloque de datos CrearRegistro (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dd73bae-a8d5-4d8b-b356-01ac72f7e5d9
description: Puede utilizar el bloque de datos CrearRegistro para crear un nuevo registro en la tabla especificada.
ms.openlocfilehash: dc4be7653081c7c02426d84c74b7b56e597706fa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815364"
---
# <a name="createrecord-data-block-access-custom-web-app"></a>Bloque de datos CrearRegistro (aplicación web personalizado de Access)

Puede utilizar el bloque de datos **CrearRegistro** para crear un nuevo registro en la tabla especificada. 
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
> [!NOTE]
> [!NOTA] El bloque de datos **CrearRegistro** solo está disponible en macros de datos. 
  
## <a name="setting"></a>Valores

El bloque de datos **CrearRegistro** tiene los siguientes argumentos. 
  
El bloque de datos **CrearRegistro** tiene los siguientes argumentos. 
  
|**Nombre del argumento**|**Necesario**|**Descripción**|
|:-----|:-----|:-----|
|**Crear un registro en ** <br/> |Sí  <br/> |Nombre de la tabla en la que se creará el nuevo registro.  <br/> |
|**Alias** <br/> |No  <br/> |Una cadena que identifica el registro. Puede utilizar el alias del registro para identificar  <br/> |
   
## <a name="remarks"></a>Comentarios

El registro creado por **CrearRegistro** se convierte automáticamente en el registro actual. 
  
Después de la instrucción de **CrearRegistro** , puede insertar un bloque de comandos que se ejecutará antes de confirmar el nuevo registro. Las acciones siguientes están disponibles en un bloque de datos **CrearRegistro**. 
  
||
|:-----|
|[CancelarCambioDeRegistro (acción de macro)](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[Comentario (instrucción de macro)](comment-macro-block-access-custom-web-app.md) <br/> |
|[Grupo (instrucción de macro)](group-macro-block-access-custom-web-app.md) <br/> |
|[If... A continuación... Instrucción de Macro Else](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[EstablecerCampo (acción de macro)](setfield-macro-action-access-custom-web-app.md) <br/> |
|[EstablecerVariableLocal (acción de macro)](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
Después de que la acción **CrearRegistro** cree un registro, utilice la acción **EstablecerCampo** para especificar un valor de un campo en el nuevo registro. 
  
Puede usar un **Si... A continuación... Else** instrucción para realizar operaciones en función de una condición. 
  
Para cancelar la creación de un registro, utilice la acción **CancelarCambioDeRegistro**. Esto evita que se confirmen los cambios y permite salir del bloque de datos **CrearRegistro**. 
  
Una vez que se confirma el nuevo registro, puede utilizar la variable local **ÚltimaIdentidadDeRegistroCreada** para trabajar con el registro. Por ejemplo, use la siguiente sintaxis para hacer referencia al campo AssignedTo del registro creado más recientemente. 
  
`[LastCreateRecordIdentity].[AssignedTo]`


