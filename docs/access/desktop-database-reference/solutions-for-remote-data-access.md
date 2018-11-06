---
title: Soluciones para el acceso remoto a datos
TOCTitle: Solutions for Remote Data Access
ms:assetid: ae84c05a-cf9b-2b4c-4d7a-e6c9dcd120c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249825(v=office.15)
ms:contentKeyID: 48547072
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ef617f91aa6f36969932a4d8f2914df2de935787
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998164"
---
# <a name="solutions-for-remote-data-access"></a>Soluciones para el acceso remoto a datos

**Se aplica a**: Access 2013, Office 2013

## <a name="the-issue"></a>El problema

ADO habilita la aplicación para obtener acceso directo y modificar orígenes de datos (a veces se denomina sistema de dos niveles). Por ejemplo, si hay una conexión con el origen de datos que contiene los datos, se trata de una conexión directa en un sistema de dos niveles.

Sin embargo, es posible que desee tener acceso a orígenes de datos indirectamente a través de un intermediario, como Microsoft Internet Information Services (IIS). Esto se denomina a veces un sistema de tres niveles. IIS es un sistema de cliente/servidor que permite de manera eficaz que una aplicación local o de cliente invoque un programa remoto o de servidor a través de Internet o una intranet. El programa de servidor obtiene acceso al origen de datos y procesa opcionalmente los datos adquiridos.

Por ejemplo, la página Web de intranet contiene una aplicación escrita en Microsoft Visual Basic Scripting Edition (VBScript), que se conecta a IIS. IIS se conecta a su vez al origen de datos real, recupera los datos, los procesa de alguna manera y, a continuación, devuelve la información procesada a la aplicación.

En este ejemplo, la aplicación no se ha conectado en ningún momento directamente al origen de datos. IIS se ha encargado de esa conexión y ha obtenido acceso a los datos por medio de ADO.

> [!NOTE]
> La aplicación de cliente/servidor no tiene que estar basado en Internet o una intranet (es decir, basada en web), podría constar únicamente de programas compilados en una red de área local. Sin embargo, el caso típico es una aplicación basada en web.

Dado que algunos controles visuales, como una cuadrícula, una casilla de verificación o una lista, pueden utilizar la información devuelta, ésta debe ser fácilmente utilizable por los controles visuales.

Desea disponer de una interfaz de programación de aplicaciones simple y eficaz que admita sistemas de tres niveles y devuelva la información con la misma facilidad con la que se recupera en un sistema de dos niveles. El servicio de datos remotos (RDS) es esta interfaz.

## <a name="the-solution"></a>La solución

RDS define un modelo de programación: la secuencia de actividades necesarias para obtener acceso y actualizar un origen de datos: para obtener acceso a datos a través de un intermediario, como Internet Information Services (IIS). El modelo de programación resume toda la funcionalidad de RDS.

