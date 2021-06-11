---
title: CALLTHIS (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251403
localization_priority: Normal
ms.assetid: 461abfc1-d2cc-2354-1c2f-395c9e351a78
description: Llama a un procedimiento en un proyecto de Microsoft Visual Basic para Aplicaciones (VBA).
ms.openlocfilehash: 7e0f0bafa39d6c1eb1fd39535506981c937ce8a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413818"
---
# <a name="callthis-function"></a>Función CALLTHIS

Llama a un procedimiento en un proyecto de Microsoft Visual Basic para Aplicaciones (VBA).
  
## <a name="syntax"></a>Sintaxis

CALLTHIS(" ** *procedure* ** ",[" ** *project* ** "],[ ** *arg1* **, ** *arg2* **,...]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _procedimiento_ <br/> |Obligatorio  <br/> |**String** <br/> | Nombre del procedimiento al que se llama.  <br/> |
| _proyecto_ <br/> |Opcional  <br/> |**String** <br/> |Proyecto que contiene el procedimiento.  <br/> |
| _arg_ <br/> |Opcional  <br/> |**Number, String, Date o Currency** <br/> |Pasa como parámetro al procedimiento.  <br/> |
   
## <a name="remarks"></a>Comentarios

En el proyecto VBA,  *el procedimiento*  se define de la siguiente manera: 
  
procedure(*vsoShape* As Visio. Shape [arg1 As type, arg2 As type...]) 
  
donde  *vsoShape*  es una referencia al **objeto Shape** que contiene la fórmula CALLTHIS que se evalúa, y  _arg1_,  *arg2*  ... son los argumentos especificados en esa fórmula. 
  
Observe que  *vsoShape*  es muy parecido al argumento "this" pasado a un procedimiento de miembro de C++; por lo tanto, el nombre "CALLTHIS". En efecto, una celda que contiene una fórmula que incluye CALLTHIS puede leerse como" Llamar a este procedimiento y pasarle una referencia a mi forma". 
  
Si _se_ especifica project, Microsoft Visio examina todos los documentos  abiertos para el que contiene el proyecto y el procedimiento _de_ llamadas en ese proyecto. Si _se_ omite project o null (""),  Visio supone que el procedimiento está en el proyecto VBA del documento que contiene la fórmula CALLTHIS que se está evaluando. 
  
Los números  _de arg1,_  _arg2..._ se pasan en unidades externas. Por ejemplo, si pasa el valor de la celda Height de una forma de 3 cm de alto, el valor transferido será 3. Para pasar unidades distintas junto con un número, debe utilizar la función FORMATEX o agregar un conjunto de valor nulo y unidad para forzar explícitamente las unidades, por ejemplo 0 cm + Height. 
  
El segundo separador (punto y coma) de la función CALLTHIS es opcional. Se corresponde con el número de parámetros adicionales agregados al procedimiento. Si no usa ningún parámetro adicional, excepto , no agregue la segunda  `(vsoShape as Visio.Shape)` coma; use CALLTHIS("",). Si agrega dos parámetros adicionales, por ejemplo, debe utilizar CALLTHIS("";;;). 
  
La función CALLTHIS siempre se evalúa en  0 y la llamada al procedimiento se produce durante el tiempo de inactividad después de que finalice el proceso de recálculo.  _El_ procedimiento puede devolver un valor, Visio omite.  _Procedure_ devuelve un valor que Visio puede reconocer estableciendo la fórmula o el resultado de otra celda del documento, pero no la celda que llamó al procedimiento _,_ a menos que desee sobrescribir la fórmula CALLTHIS.
  
La función CALLTHIS se diferencia de la función RUNADDON en que no es necesario que el proyecto de un documento haga referencia a otro proyecto para que se pueda llamar a ese proyecto. 
  
> [!NOTE]
>  El código VBA que se invoca cuando una copia de Visio evalúa una función CALLTHIS que forma parte de una fórmula no debe cerrar el documento que contiene la celda que utiliza la función, ya que, de hacerlo, se producirá un error de aplicación y la ejecución de Visio se terminará. 
  
Si necesita cerrar el documento que contiene la celda que usa la función CALLTHIS, puede usar uno de los métodos siguientes: 
  
- Cerrar el documento mediante código que no sea de VBA.
    
- Cerrar el documento desde un proyecto diferente al que se cierra.
    
- Enviar mensajes de ventana para cerrar las ventanas del documento en lugar de cerrar el documento.
    
Para obtener más información sobre cómo ejecutar código en Visio, vea [Acerca de la configuración de seguridad y la ejecución de código en Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) en esta Referencia de ShapeSheet. 
  
## <a name="example-1"></a>Ejemplo 1

CALLTHIS("p";;FORMATEX(Height;"#,00 u";;"cm"))
  
Llama a un procedimiento denominado p que se encuentra en un módulo y le pasa el valor de Height en centímetros, por ejemplo 7,62 cm.
  
## <a name="example-2"></a>Ejemplo 2

CALLTHIS("q",,0 cm.+Height,Width)
  
Llama a un procedimiento denominado q que se encuentra en un módulo y le pasa el alto de la celda en centímetros y el ancho en unidades internas.
  
## <a name="example-3"></a>Ejemplo 3

Use el siguiente procedimiento en el *módulo de clase ThisDocument.* 
  
Utilice alguna de las sintaxis siguientes en la celda EventDblClick de una forma con los procedimientos anteriores.
  
CALLTHIS("ThisDocument.A",)
  
CALLTHIS("ThisDocument.B","Click")
  
CALLTHIS("ThisDocument.C",,"Click", " OK.")
  

