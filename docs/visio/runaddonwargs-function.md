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
description: Ejecuta cadena y le pasa los argumentos de línea de comandos para el programa como una cadena.
ms.openlocfilehash: 7bc05a0cbf32550d1e39bee39bec83101882cf19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823093"
---
# <a name="runaddonwargs-function"></a>RUNADDONWARGS (función)

Ejecuta _cadena_ y le pasa los _argumentos_ de línea de comandos para el programa como una cadena. 
  
## <a name="syntax"></a>Sintaxis

RUNADDONWARGS ("** *cadena* **","** *argumentos* **") 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _string_ <br/> |Obligatorio  <br/> |**String** <br/> | Nombre de un complemento.  <br/> |
| _argumentos_ <br/> |Obligatorio  <br/> |**String** <br/> |Argumentos por pasar al programa.  <br/> |
   
## <a name="remarks"></a>Observaciones

En la práctica, _los argumentos_ deben ser 50 o menos caracteres. Utilice la función RUNADDONWARGS para enlazar un programa, como un complemento a una celda, por ejemplo, a una celda Action o Events. 
  
La función RUNADDONWARGS sólo puede ejecutar complementos que son miembros de la colección **Addons** de la aplicación. Para estar presente en la colección, un complemento debe ser un archivo EXE o VSL que es: 
  
- Instalado en la ruta de acceso de **Inicio** o **Addons** de la aplicación. 
    
- Agregar mediante programación utilizando el método **Add** de la colección **Addons** . 
    
Para obtener más información acerca de cómo ejecutar código en Visio, vea [acerca de la configuración de seguridad y la ejecución de código en Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) en esta referencia de ShapeSheet. 
  
En versiones anteriores de Visio, esta función se denominaba _RUNADDONWARGS. La versión 4.0 de Visio y las posteriores aceptan cualquiera de las dos denominaciones.
  
## <a name="example"></a>Ejemplo

RUNADDONWARGS ("GRAPHMKR. EXE"," / GraphMaker = Stack ") 
  
Inicia el complemento Graphmkr.exe y le pasa el argumento /GraphMaker=Stack. 
  

