---
title: Funciones seguras para clústeres
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 787badaf-8782-454d-a016-7eae83bbd8a9
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d32925fcd5c3be7fe3e615ee2290f25c7595911c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409303"
---
# <a name="cluster-safe-functions"></a>Funciones seguras para clústeres

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
En Excel 2013, Excel puede descargar llamadas de función definidas por el usuario (UDF) a un clúster de cómputo de alto rendimiento a través de una interfaz de conector de clúster dedicado. Los proveedores de clústeres de cómputo proporcionan conectores de clúster. Los autores de FDU pueden declarar sus FDU como un clúster seguro y, cuando un conector del clúster está presente, Excel envía las llamadas a estas UDF al conector del clúster para la descarga.
  
Cuando Excel detecta una UDF segura para clúster durante la actualización, pasa el nombre del XLL que se está ejecutando actualmente, el nombre de la UDF segura para clúster y los parámetros del conector de clúster. El conector ejecuta la llamada a UDF de forma remota y devuelve los resultados a Excel. El cálculo no dependiente continúa y cuando el conector del clúster ha terminado de ejecutar la UDF, pasa los resultados a Excel y los cálculos dependientes continúan. El mecanismo de este comportamiento asincrónico imita el mecanismo que usan las UDF asincrónicas, excepto que el conector de clúster administra los aspectos asincrónicos en lugar del autor de la UDF. Normalmente, un conector de clúster implementa una corrección de XLL para cargar los XLL y ejecutar las UDF en los nodos de clúster de cálculo.
  
La mecánica de declaración de las UDF como seguras para clústeres es similar a la de declarar las UDF como seguras para la actualización multiproceso. Sin embargo, dado que la UDF no se está ejecutando necesariamente en el mismo equipo que otras UDF desde la misma sesión de Excel, existen diferentes consideraciones a la hora de escribir UDF seguras para clústeres.
  
Para registrar una UDF como segura para clústeres, debe llamar a la función de devolución de llamada [xlfRegister (Form 1)](xlfregister-form-1.md) a través de la interfaz **Excel12** o **Excel12v** . Para obtener más información acerca de estas interfaces, consulte [Excel4/Excel12](excel4-excel12.md) y [Excel4v/Excel12v](excel4v-excel12v.md). No se admite el registro de un UDF como seguro para clúster a través de la interfaz de **Excel4** o **Excel4v** . 
  
Si registra una función como segura para clústeres, debe asegurarse de que la función se comporta de forma segura para clústeres. Aunque el comportamiento exacto del conector de clúster es específico de la implementación, debe diseñar la UDF para que se ejecute en un sistema de equipo distribuido y para que tenga las siguientes características:
  
- Una FDU no debe confiar en ningún estado de la memoria. Por ejemplo, una UDF no debe basarse en una memoria caché existente en la memoria.
    
- Una UDF no debe realizar devoluciones de llamada de Excel que no son compatibles con el proveedor de conectores de clúster.
    
Además del comportamiento seguro para clústeres, existen las siguientes restricciones técnicas en las UDF seguras para clústeres:
  
1. No hay argumentos XLOPER (Types ' P ', ' R ').
    
2. No hay argumentos XLOPER12 que admitan referencias de rango (tipo ' U ').
    
3. No puede ser una función equivalente de hoja de macros ('&amp;# ' y ' ' no se puede combinar).
    
Para los archivos UDF con tiempos de ejecución más cortos, la sobrecarga de la descarga puede ser mayor que el tiempo que se tarda en ejecutar la UDF, con lo que se niegan muchas de las ventajas de usar esta infraestructura.
  
> [!NOTE]
> No se puede declarar una UDF segura para clúster como UDF asincrónica. 
  
Una UDF puede determinar si se está ejecutando con un conector de clúster mediante una llamada a la función de devolución de llamada [xlRunningOnCluster](xlrunningoncluster.md) . 
  

