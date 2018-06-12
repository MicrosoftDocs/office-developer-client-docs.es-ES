---
title: Acción de SetReturnVar Macro (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 57965c84-7a52-4d7c-9c7f-be3d4570576d
description: La acción SetReturnVar crea una variable de retorno y establece en un valor específico.
ms.openlocfilehash: d0638c8f1e3b184a7c685ad8649c8923bdfd8f50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815512"
---
# <a name="setreturnvar-macro-action-access-custom-web-app"></a>Acción de SetReturnVar Macro (aplicación web personalizado de Access)

La acción **SetReturnVar** crea una variable de retorno y establece en un valor específico. 
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
> [!NOTE]
> La acción **SetReturnVar** sólo está disponible en Macros de datos. 
  
## <a name="setting"></a>Configuración

La acción **SetReturnVar** tiene los siguientes argumentos. 
  
|**Nombre del argumento**|**Necesario**|**Descripción**|
|:-----|:-----|:-----|
| _Name_ <br/> |Sí  <br/> |Una cadena que especifica el nombre de la variable.  <br/> |
| _Expression_ <br/> |Sí  <br/> |Una expresión que se usará para establecer el valor de esta variable temporal. Delante de la expresión con el signo igual (=). Puede hacer clic en el botón **Generar** para usar el **Generador de expresiones** para definir este argumento.  <br/> |
   
## <a name="remarks"></a>Notas

La acción **SetReturnVar** se usa para crear un **ReturnVar**, que es la variable que se puede utilizar las macros que llaman a una macro de datos mediante el uso de la acción **EjecutarMacroDeDatos** . 
  
Una vez creado un **ReturnVar** por la acción **SetReturnVar** , la macro llamada puede usar en una expresión. Por ejemplo, si ha creado un **ReturnVar** denominado **UpdateSuccess**, podría usar la variable utilizando la sintaxis siguiente:
  
`=[ReturnVars]![UpdateSuccess]`

La acción **SetReturnVar** se puede usar en macros de datos con nombre. No está disponible en macros de datos que están asociadas a un evento de macro de datos. 
  

