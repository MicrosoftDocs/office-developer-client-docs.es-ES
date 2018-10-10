---
title: Utilizar ADO con lenguajes de secuencias de comandos
TOCTitle: Using ADO with Scripting Languages
ms:assetid: 2e163ffb-22fe-36f5-9960-8f6bcb148183
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249074(v=office.15)
ms:contentKeyID: 48543985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2de5cd9507ede3308a207b078a5bc66a4917e267
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486663"
---
# <a name="using-ado-with-scripting-languages"></a>Utilizar ADO con lenguajes de secuencias de comandos


**Se aplica a**: Access 2013 | Office 2013

En un entorno de scripting, ADO permite exponer datos mediante scripting de servidor. En este escenario, ADO, el proveedor OLE DB subyacente que usa y cualquier otro componente necesario para hacer referencia a un almacén de datos determinado están instalados en un servidor que ejecuta Internet Information Services(IIS). Con páginas Active Server (ASP), ADO es un componente al que se hace referencia en un script que puede generar, por ejemplo, contenido HTML. Este contenido HTML se puede pasar a un explorador web de cliente a través de HTTP. En un entorno de scripting, ADO permite exponer datos mediante scripting de servidor. En este escenario, se instala en un servidor con Internet Information Services (IIS): ADO, el proveedor OLE DB subyacente que usa, y muchos otros componentes necesarios para hacer referencia a un determinado almacén de datos. ADO, que usa páginas Active Server (ASP), es un componente al que se hace referencia en un script que puede generar HTML, por ejemplo. Este contenido HTML se puede pasar mediante HTTP a un explorador web de cliente. Mediante el uso de scripting, la página web puede enviar acciones al script de servidor, lo que permite actualizar, atravesar o consultar datos específicos.

## <a name="odbc-data-sources"></a>Orígenes de datos ODBC

Una diferencia importante entre código de ADO que consta de secuencias de comandos y código de ADO que no consta de secuencias de comandos es el origen de datos ODBC, en caso de que se utilice. Para las aplicaciones que no sean secuencias de comandos, se puede crear un DSN de usuario en el Administrador de orígenes de datos ODBC. Para las secuencias de comandos que se ejecutan en IIS, debe crear un DSN de sistema; en caso contrario, las secuencias de comandos no reconocerán el origen de datos creado. Esto se aplica a cualquier aplicación de secuencias de comandos de ADO que utilice el proveedor de Microsoft OLE DB para ODBC a través de Microsoft IIS.

## <a name="referencing-the-ado-library"></a>Hacer referencia a la biblioteca de ADO

No está disponible con los lenguajes de secuencias de comandos.

## <a name="handling-events"></a>Controlar eventos

No está disponible con los lenguajes de secuencias de comandos.

Los temas siguientes contienen información más específica sobre la utilización de ADO con los lenguajes de secuencias de comandos:

  - [ADO en VBScript](vbscript-ado-programming.md)

  - [ADO en JScript](jscript-ado-programming.md)

