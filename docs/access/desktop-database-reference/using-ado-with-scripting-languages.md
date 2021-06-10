---
title: Utilizar ADO con lenguajes de secuencias de comandos
TOCTitle: Using ADO with Scripting Languages
ms:assetid: 2e163ffb-22fe-36f5-9960-8f6bcb148183
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249074(v=office.15)
ms:contentKeyID: 48543985
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1ab0615d1c16900e86a844635fad4ac9a90751a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312046"
---
# <a name="using-ado-with-scripting-languages"></a>Uso de ADO con lenguaje de scripting


**Se aplica a:** Access 2013, Office 2013

Dentro de un entorno de scripting, ADO permite exponer datos mediante scripting del lado servidor. En este escenario, ADO, el proveedor OLE DB subyacente que usa, y cualquier otro componente necesario para hacer referencia a un almacén de datos determinado se instala en un servidor que ejecuta Internet Information Services (IIS). Con páginas Active Server (ASP), ADO es un componente al que se hace referencia en un script que puede generar HTML, por ejemplo. Este contenido HTML se puede pasar a través de HTTP a un explorador web cliente. Mediante el uso de scripts, la página web puede enviar acciones de vuelta al script del lado servidor, lo que le permite actualizar, recorrer o ver datos específicos.

## <a name="odbc-data-sources"></a>Orígenes de datos ODBC

Una diferencia importante entre código de ADO que consta de secuencias de comandos y código de ADO que no consta de secuencias de comandos es el origen de datos ODBC, en caso de que se utilice.

Para las aplicaciones que no sean secuencias de comandos, se puede crear un DSN de usuario en el Administrador de orígenes de datos ODBC.

Para las secuencias de comandos que se ejecutan en IIS, debe crear un DSN de sistema; en caso contrario, las secuencias de comandos no reconocerán el origen de datos creado.

Esto se aplica a cualquier aplicación de secuencias de comandos de ADO que utilice el proveedor de Microsoft OLE DB para ODBC a través de Microsoft IIS.

## <a name="referencing-the-ado-library"></a>Hacer referencia a la biblioteca de ADO

No está disponible con los lenguajes de secuencias de comandos.

## <a name="handling-events"></a>Controlar eventos

No está disponible con los lenguajes de secuencias de comandos.

Los temas siguientes contienen información más específica sobre la utilización de ADO con los lenguajes de secuencias de comandos:

- [Programación ADO con JScript](jscript-ado-programming.md)

- [Programación ADO en VBScript](vbscript-ado-programming.md)
