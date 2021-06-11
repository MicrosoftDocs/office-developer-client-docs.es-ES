---
title: Desarrollo de Excel conectores de clúster
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
# <a name="developing-excel-cluster-connectors"></a>Desarrollo de Excel conectores de clúster

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Excel conectores de clúster proporcionan un medio para descargar automáticamente las llamadas de función definidas por el usuario seguras para clústeres en un XLL a un servidor agrupado. Para obtener una descripción de las funciones definidas por el usuario seguras para clústeres, [vea Cluster Caja fuerte Functions](cluster-safe-functions.md). Esta descarga puede mejorar el rendimiento al permitir el uso de más recursos informáticos. Normalmente, un proveedor de clústeres de proceso de alto rendimiento desarrolla un conector de clúster.
  
## <a name="cluster-connectors"></a>Conectores de clúster

Un conector de clúster es un DLL que proporciona puntos de entrada definidos que Excel para coordinar llamadas de función definidas por el usuario seguras para clústeres. Sirve como interfaz entre Excel y el clúster de cálculo de alto rendimiento, para la administración de sesiones, para realizar llamadas de función (pasando el nombre de función completo y los argumentos reales de la llamada) y para devolver los resultados de llamadas a Excel mediante un mecanismo de devolución de llamada.
  
Para crear un conector de clúster, cree un ARCHIVO DLL que exponga los puntos de entrada enumerados [en Excel cluster Connector Functions](excel-cluster-connector-functions.md).
  
## <a name="installing-a-cluster-connector"></a>Instalación de un conector de clúster

Para que un conector de clúster esté disponible en Excel, el código de instalación del conector debe instalar la DLL del conector en el equipo donde Excel está instalado. Además, el código de instalación del conector debe agregar una entrada para el conector bajo la siguiente clave del Registro:
  
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors\
  
Agregue un nodo a esta clave para el conector de clúster que especifique las cadenas siguientes:
  
-  `Name`— el nombre que aparecerá en la lista de conectores de clúster en Excel.
    
-  `Filename`— la ruta de acceso completa para la DLL.
    

