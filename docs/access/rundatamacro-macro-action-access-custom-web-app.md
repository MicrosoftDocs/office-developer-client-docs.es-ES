---
title: Acción de Macro EjecutarMacroDeDatos (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f6010ac5-6c08-4c1b-a811-ff81b30ed5f0
description: Puede usar la acción EjecutarMacroDeDatos para ejecutar una macro de datos independientes.
ms.openlocfilehash: 55a0ff4c731dc517c5d71aa20d8e46c3b4ff4611
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815480"
---
# <a name="rundatamacro-macro-action-access-custom-web-app"></a>Acción de Macro EjecutarMacroDeDatos (aplicación web personalizado de Access)

Puede usar la acción **EjecutarMacroDeDatos** para ejecutar una macro de datos independientes. 
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="setting"></a>Configuración

La acción **EjecutarMacroDeDatos** tiene el siguiente argumento. 
  
|**Argumento de la acción**|**Descripción**|
|:-----|:-----|
| _Nombre de macro_ <br/> |Nombre de la macro de datos que se va a ejecutar.  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando selecciona la macro de datos que desea ejecutar en el Diseñador de macros, Access determina si la macro de datos requiere parámetros. Si la macro de datos requiere parámetros, se mostrarán cuadros de texto que se puede escribir en los argumentos.
  
Cuando se ejecuta una macro que contiene la acción **EjecutarMacroDeDatos** y se llega a la acción **EjecutarMacroDeDatos**, Access ejecuta la macro de datos a la que se ha llamado. Cuando esta macro de datos termina, Access vuelve a la macro original y ejecuta la acción siguiente. 
  

