---
title: HYPERLINK (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251441
localization_priority: Normal
ms.assetid: 943636a6-e135-a626-7924-11e238156548
description: Se desplaza a la dirección especificada, que puede ser un archivo, UNC o dirección URL de ruta de acceso.
ms.openlocfilehash: 5e4952c3d56eff0cb1e6518928a7b8259f645046
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401079"
---
# <a name="hyperlink-function"></a>Función HYPERLINK

Se desplaza a la dirección especificada, que puede ser un archivo, UNC o dirección URL de ruta de acceso.
  
## <a name="syntax"></a>Sintaxis

HYPERLINK ("** *dirección* **" ["," ** *subaddress* ** "," ** *extrainfo* ** ", ** *ventana* **," ** *marco* ** "]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _dirección_ <br/> |Obligatorio  <br/> |**String** <br/> |Ruta de acceso completa o relativa.  <br/> |
| _subdirección_ <br/> |Opcional  <br/> |**String** <br/> |Especifica la ubicación, dentro de la dirección especificada, con la que debe establecerse el vínculo. Por ejemplo, si dirección es un archivo de Microsoft Visio, subdirección puede ser un nombre de página. Si se trata de un archivo de Microsoft Excel, subdirección puede ser una hoja de cálculo o un rango de celdas en ella. Si se trata de la dirección URL de una página HTML, la subdirección puede ser un delimitador.  <br/> |
| _ExtraInfo_ <br/> |Opcional  <br/> |**String** <br/> |Pasa información que se usa en una dirección URL, como las coordenadas de un mapa de imagen.  <br/> |
| _ventana_ <br/> |Opcional  <br/> |**Boolean** <br/> |Especifica si el hipervínculo se debe abrir o no en una ventana nueva. El valor predeterminado es FALSE.  <br/> |
| _marco_ <br/> |Opcional  <br/> |**String** <br/> | Especifica el nombre de un marco de destino cuando Visio se abre como un documento Active en un explorador ActiveX, por ejemplo, en Microsoft Internet Explorer 3.0 o posterior. El valor predeterminado es una cadena vacía.  <br/> |
   
## <a name="remarks"></a>Observaciones

Si el documento no tiene ruta de acceso base, Visio se desplaza siguiendo la ruta de acceso del documento. Si no se ha guardado el documento, el hipervínculo no está definido. 
  
Las rutas de acceso relativas basadas en el campo **Base de hipervínculo** especificado en el cuadro de diálogo **Propiedades de Visio**. 
  
Se puede usar la función GOTOPAGE para desplazarse a las páginas de un documento. 
  
## <a name="example-1"></a>Ejemplo 1

 `HYPERLINK("C:\My Documents\Drawing1.vsdx")`
  
## <a name="example-2"></a>Ejemplo 2

 `HYPERLINK("\\Server\Share\Drawing1.vsdx")`
  
## <a name="example-3"></a>Ejemplo 3

 `HYPERLINK("https://www.microsoft.com")`
  
## <a name="example-4"></a>Ejemplo 4

 `HYPERLINK("..\data.xlsx","sheet1!A1")`
  

