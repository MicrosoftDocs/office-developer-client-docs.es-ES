---
title: RUNADDONWARGS (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251493
localization_priority: Normal
ms.assetid: c154413f-c366-a66b-94e3-ed71ad23f325
description: Ejecuta la cadena y pasa los argumentos de la línea de comandos al programa como una cadena.
ms.openlocfilehash: bc05a4480438875c348373059f57bf04f82c9eca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318952"
---
# <a name="runaddonwargs-function"></a>Función RUNADDONWARGS

Ejecuta la _cadena_ y pasa los _argumentos_ de la línea de comandos al programa como una cadena. 
  
## <a name="syntax"></a>Sintaxis

RUNADDONWARGS ("* * *cadena* * *", "* * *argumentos* * *") 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _string_ <br/> |Obligatorio  <br/> |**String** <br/> | Nombre de un complemento.  <br/> |
| _argumentos_ <br/> |Obligatorio  <br/> |**String** <br/> |Argumentos por pasar al programa.  <br/> |
   
## <a name="remarks"></a>Comentarios

En la práctica, los _argumentos_ deben ser de 50 o menos caracteres. Utilice la función RUNADDONWARGS para enlazar un programa, por ejemplo un complemento, a una celda (por ejemplo, a una celda Action o Events). 
  
La función RUNADDONWARGS sólo puede ejecutar complementos que son miembros de la colección Addons **** de la aplicación. Para estar presente en esa colección, un complemento debe ser un archivo EXE o un archivo VSL que: 
  
- Instalado en la ruta **Startup** o **Addons** de la aplicación. 
    
- Programado mediante el método **Add** de la colección **Addons**. 
    
Para obtener más información acerca de cómo ejecutar código en Visio, vea [Acerca de la configuración de seguridad y la ejecución de código en Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) en esta Referencia de ShapeSheet. 
  
En versiones anteriores de Visio, esta función se denominaba _RUNADDONWARGS. La versión 4.0 de Visio y las posteriores aceptan cualquiera de las dos denominaciones.
  
## <a name="example"></a>Ejemplo

RUNADDONWARGS ("GRAPHMKR. EXE ","/GraphMaker = stack ") 
  
Inicia el complemento Graphmkr.exe y le pasa el argumento /GraphMaker=Stack. 
  

