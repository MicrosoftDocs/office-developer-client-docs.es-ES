---
title: Desarrollo de conectores de clúster de Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b538ae44-37d2-496b-b6e7-b0e39f6e38cb
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e1c70713586a7a143f119a2c3e9d34b982dcedba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412600"
---
# <a name="developing-excel-cluster-connectors"></a>Desarrollo de conectores de clúster de Excel

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Los conectores de clúster de Excel proporcionan un medio para descargar automáticamente las llamadas de funciones definidas por el usuario seguras para clústeres en un XLL a un servidor agrupado. Para obtener una descripción de las funciones definidas por el usuario seguras para clústeres, consulte [cluster Safe Functions](cluster-safe-functions.md). Esta descarga puede mejorar el rendimiento al permitir que se usen más recursos informáticos. Un conector de clúster suele ser desarrollado por un proveedor de clústeres de cómputo de alto rendimiento.
  
## <a name="cluster-connectors"></a>Conectores de clúster

Un conector de clúster es una DLL que proporciona puntos de entrada definidos que Excel usa para coordinar llamadas de función definidas por el usuario seguras para clústeres. Actúa como una interfaz entre Excel y el clúster de cómputo de alto rendimiento, para la administración de sesiones, para realizar llamadas de función (pasando el nombre completo de la función y los argumentos reales de la llamada) y devolver los resultados de la llamada a Excel a través de un mecanismo de devolución de llamada.
  
Para crear un conector de clúster, cree un archivo DLL que exponga los puntos de entrada enumerados en [funciones de conector de clúster de Excel](excel-cluster-connector-functions.md).
  
## <a name="installing-a-cluster-connector"></a>Instalación de un conector de clúster

Para que un conector de clúster esté disponible en Excel, el código del programa de instalación del conector debe instalar la DLL del conector en el equipo en el que está instalado Excel. Además, el código del programa de instalación del conector debe agregar una entrada para el conector en la siguiente clave del registro:
  
Conectores de clúster de HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel \
  
Agregue un nodo a esta clave para el conector de clúster que especifica las siguientes cadenas:
  
-  `Name`: el nombre que aparecerá en la lista de conectores de clúster en Excel.
    
-  `Filename`: la ruta de acceso completa del archivo DLL.
    

