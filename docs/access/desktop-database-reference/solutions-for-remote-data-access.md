---
title: Soluciones para el acceso remoto a datos
TOCTitle: Solutions for Remote Data Access
ms:assetid: ae84c05a-cf9b-2b4c-4d7a-e6c9dcd120c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249825(v=office.15)
ms:contentKeyID: 48547072
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 45164401bbab5cc9134fa7a354fde54bbb02fa37
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604788"
---
# <a name="solutions-for-remote-data-access"></a>Soluciones para el acceso remoto a datos


**Se aplica a**: Access 2013 | Office 2013

## <a name="the-issue"></a>Problema

ADO habilita la aplicación para obtener acceso directo y modificar orígenes de datos (a veces se denomina sistema de dos niveles). Por ejemplo, si hay una conexión con el origen de datos que contiene los datos, se trata de una conexión directa en un sistema de dos niveles.

Sin embargo, es posible que desee obtener indirectamente acceso a los orígenes de datos a través de un intermediario como Internet Information Services de Microsoft® (IIS). Esto se denomina a veces un sistema de tres niveles. IIS es un sistema de cliente/servidor que permite de manera eficaz que una aplicación local o de cliente invoque un programa remoto o de servidor a través de Internet o una intranet. El programa de servidor obtiene acceso al origen de datos y procesa opcionalmente los datos adquiridos.

<<<<<<< HEAD para el ejemplo, la página Web de intranet contiene una aplicación escrita en Microsoft® Visual Basic Scripting Edition (VBScript), que se conecta a IIS. IIS se conecta a su vez al origen de datos real, recupera los datos, los procesa de alguna manera y, a continuación, devuelve la información procesada a la aplicación.
=== Por ejemplo, la página Web de intranet contiene una aplicación escrita en Microsoft® Visual Basic Scripting Edition (VBScript), que se conecta a IIS. IIS se conecta a su vez al origen de datos real, recupera los datos, los procesa de alguna manera y, a continuación, devuelve la información procesada a la aplicación.
>>>>>>> master

En este ejemplo, la aplicación no se ha conectado en ningún momento directamente al origen de datos. IIS se ha encargado de esa conexión y ha obtenido acceso a los datos por medio de ADO.


> [!NOTE]
> <P>[!NOTA] La aplicación de cliente/servidor no debe estar ubicada en Internet o una intranet (es decir, basada en Web). Puede constar únicamente de programas compilados en una red local. Sin embargo, normalmente se trata de una aplicación basada en Web.</P>



Dado que algunos controles visuales, como una cuadrícula, una casilla de verificación o una lista, pueden utilizar la información devuelta, ésta debe ser fácilmente utilizable por los controles visuales.

Desea disponer de una interfaz de programación de aplicaciones simple y eficaz que admita sistemas de tres niveles y devuelva la información con la misma facilidad con la que se recupera en un sistema de dos niveles. El servicio de datos remotos (RDS) es esta interfaz.

## <a name="the-solution"></a>Solución

RDS define un modelo de programación (es decir, la secuencia de actividades necesarias para obtener acceso y actualizar un origen de datos) para obtener acceso a datos a través de un intermediario, como Internet Information Services (IIS). El modelo de programación resume toda la funcionalidad de RDS.

