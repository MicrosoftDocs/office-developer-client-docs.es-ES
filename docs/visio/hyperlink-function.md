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
description: Navega a la dirección especificada, que puede ser una ruta de acceso de archivo, UNC o DIRECCIÓN URL.
ms.openlocfilehash: 5e4952c3d56eff0cb1e6518928a7b8259f645046
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329949"
---
# <a name="hyperlink-function"></a>Función HYPERLINK

Navega a la dirección especificada, que puede ser una ruta de acceso de archivo, UNC o DIRECCIÓN URL.
  
## <a name="syntax"></a>Sintaxis

HYPERLINK(" ** *address* ** "[," ** *subaddress* ** "," ** *extrainfo* ** ", ** *window* **," ** *frame* ** "]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _address_ <br/> |Obligatorio  <br/> |**String** <br/> |Ruta de acceso completa o relativa.  <br/> |
| _subaddress_ <br/> |Opcional  <br/> |**String** <br/> |Especifica la ubicación, dentro de la dirección especificada, con la que debe establecerse el vínculo. Por ejemplo, si dirección es un archivo de Microsoft Visio, subdirección puede ser un nombre de página. Si se trata de un archivo de Microsoft Excel, subdirección puede ser una hoja de cálculo o un rango de celdas en ella. Si se trata de la dirección URL de una página HTML, la subdirección puede ser un delimitador.  <br/> |
| _extrainfo_ <br/> |Opcional  <br/> |**String** <br/> |Pasa información que se usa en una dirección URL, como las coordenadas de un mapa de imagen.  <br/> |
| _ventana_ <br/> |Opcional  <br/> |**Boolean** <br/> |Especifica si el hipervínculo se debe abrir o no en una ventana nueva. El valor predeterminado es FALSE.  <br/> |
| _marco_ <br/> |Opcional  <br/> |**String** <br/> | Especifica el nombre de un marco de destino cuando Visio se abre como un documento Active en un explorador ActiveX, por ejemplo, en Microsoft Internet Explorer 3.0 o posterior. El valor predeterminado es una cadena vacía.  <br/> |
   
## <a name="remarks"></a>Comentarios

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
  

