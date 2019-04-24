---
title: Acción de macro RunDataMacro (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f6010ac5-6c08-4c1b-a811-ff81b30ed5f0
description: Puede usar la acción RunDataMacro para ejecutar una macro de datos independiente.
ms.openlocfilehash: 68c0e5a3837039bdab1165e686adb3bdf2a5b6f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304245"
---
# <a name="rundatamacro-macro-action-access-custom-web-app"></a>Acción de macro RunDataMacro (aplicación web personalizada de Access)

Puede usar la acción **RunDataMacro** para ejecutar una macro de datos independiente. 
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="setting"></a>Configuración

La acción **EjecutarMacroDeDatos** tiene el siguiente argumento. 
  
|**Argumento de la acción**|**Descripción**|
|:-----|:-----|
| _Nombre de macro_ <br/> |Nombre de la macro de datos que se va a ejecutar.  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando selecciona la macro de datos que desea ejecutar en el Diseñador de macros, Access determina si la macro de datos requiere parámetros. Si la macro de datos requiere parámetros, aparecerán cuadros de texto en los que puede escribir los argumentos.
  
Cuando se ejecuta una macro que contiene la acción **EjecutarMacroDeDatos** y se llega a la acción **EjecutarMacroDeDatos**, Access ejecuta la macro de datos a la que se ha llamado. Cuando esta macro de datos termina, Access vuelve a la macro original y ejecuta la acción siguiente. 
  

