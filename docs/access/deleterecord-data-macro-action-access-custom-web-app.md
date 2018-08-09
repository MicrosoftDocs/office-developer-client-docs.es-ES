---
title: Acción de Macro de datos DeleteRecord (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: f6b68a9a-e04a-476e-a407-b1779fea1953
description: Puede usar la acción EliminarRegistro para eliminar un registro.
ms.openlocfilehash: 64742d73ec57b94474c8e27822fd3946c7673336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815289"
---
# <a name="deleterecord-data-macro-action-access-custom-web-app"></a>Acción de Macro de datos DeleteRecord (aplicación web personalizado de Access)

Puede usar la acción **EliminarRegistro** para eliminar un registro. 
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="setting"></a>Configuración

La acción **DeleteRecord** tiene los siguientes argumentos. 
  
|**Argumento**|**Descripción**|
|:-----|:-----|
|**Alias del registro** <br/> |Una cadena que identifica el registro para eliminar. Si no se especifica el argumento de *Alias* , a continuación, se elimina el registro actual.  <br/> |
   
## <a name="remarks"></a>Comentarios

Puede utilizar la variable local **ÚltimaIdentidadDeRegistroCreada** para trabajar con el último registro creado en un bloque de datos **CrearRegistro**. Por ejemplo, utilice la siguiente sintaxis para hacer referencia al registro creado más recientemente: 
  
`[LastCreateRecordIdentity]`


