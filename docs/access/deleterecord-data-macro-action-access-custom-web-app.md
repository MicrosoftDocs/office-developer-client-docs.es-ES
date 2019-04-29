---
title: Acción de macro de datos DeleteRecord (aplicación web personalizada de Access)
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
# <a name="deleterecord-data-macro-action-access-custom-web-app"></a>Acción de macro de datos DeleteRecord (aplicación web personalizada de Access)

Puede usar la acción **EliminarRegistro** para eliminar un registro. 
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="setting"></a>Configuración

La acción **DeleteRecord** tiene los siguientes argumentos. 
  
|**Argumento**|**Descripción**|
|:-----|:-----|
|**Alias del registro** <br/> |Una cadena que identifica el registro que hay que eliminar. Si no se especifica el argumento *alias* , se elimina el registro actual.  <br/> |
   
## <a name="remarks"></a>Comentarios

Puede utilizar la variable local **ÚltimaIdentidadDeRegistroCreada** para trabajar con el último registro creado en un bloque de datos **CrearRegistro**. Por ejemplo, use la siguiente sintaxis para hacer referencia al registro creado más recientemente: 
  
`[LastCreateRecordIdentity]`


