---
title: RUNMACRO (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033809
localization_priority: Normal
ms.assetid: 86b0f071-5e0b-56de-ff5b-63c114ad823a
description: Llama a una macro en un proyecto de Microsoft Visual Basic para aplicaciones (VBA).
ms.openlocfilehash: 77045bd67fe9be9aab14e73199b33b93c6d70c2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355716"
---
# <a name="runmacro-function"></a>Función RUNMACRO

Llama a una macro en un proyecto de Microsoft Visual Basic para aplicaciones (VBA). 
  
## <a name="syntax"></a>Sintaxis

RunMacro (* * *nombremacro* * * [, * * *projname_opt* * *]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _nombremacro_ <br/> |Obligatorio  <br/> |**String** <br/> |Nombre de la macro por llamar.  <br/> |
| _projname_opt_ <br/> |Opcional  <br/> |**String** <br/> | Proyecto que contiene la macro.  <br/> |
   
## <a name="remarks"></a>Comentarios

Si se especifica un proyecto, Microsoft Visio explora todos los documentos abiertos para el que contiene _projname_opt_ y llama a _nombremacro_ en ese proyecto. Si se omite el _projname_opt_ o su valor es nulo (""), se supone que _nombremacro_ se encuentra en el proyecto de VBA del documento que contiene la fórmula RunMacro que se está evaluando. 
  
La función RUNMACRO se diferencia de la función CALLTHIS en que no pasa una referencia a la forma que posee la fórmula que se evalúa como _nombremacro_. Al igual que sucede con CALLTHIS, la función RUNMACRO no requiere una referencia a _projname_opt_ para llamar a ella. 
  
 El código VBA que se invoca cuando una copia de Visio evalúa una función RUNMACRO que forma parte de una fórmula no debe cerrar el documento que contiene la celda que utiliza la función, ya que, de hacerlo, se producirá un error de aplicación y la ejecución de Visio se terminará. 
  
Si necesita cerrar el documento que contiene la celda que usa la función RUNMACRO, puede usar uno de los métodos siguientes:
  
- Cerrar el documento mediante código que no sea de VBA.
    
- Cerrar el documento desde un proyecto diferente al que se cierra.
    
- Enviar mensajes de ventana para cerrar las ventanas del documento en lugar de cerrar el documento.
    
Para obtener más información acerca cómo ejecutar código en Visio, vea [Acerca de la configuración de seguridad y la ejecución de código en Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) en esta Referencia de ShapeSheet. 
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente, se invoca una macro llamada MiPrueba en el módulo de clase ThisDocument del proyecto VBA que contiene la fórmula RUNMACRO. 
  
RUNMACRO ("ThisDocument.MiPrueba") 
  

