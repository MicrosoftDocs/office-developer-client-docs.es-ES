---
title: CON declaración OWNERACCESS OPTION (Microsoft Access SQL)
TOCTitle: WITH OWNERACCESS OPTION declaration (Microsoft Access SQL)
ms:assetid: 82e51071-12b2-e97e-07b4-27ffceda831e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196724(v=office.15)
ms:contentKeyID: 48545993
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277584
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0eca4738d07c54b049073aaf5d4b802864761fa5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920602"
---
# <a name="with-owneraccess-option-declaration-microsoft-access-sql"></a><span data-ttu-id="6cfd9-102">CON declaración OWNERACCESS OPTION (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="6cfd9-102">WITH OWNERACCESS OPTION declaration (Microsoft Access SQL)</span></span>


<span data-ttu-id="6cfd9-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6cfd9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6cfd9-104">En un entorno multiusuario con un grupo de trabajo seguro, use esta declaración con una consulta para conceder al usuario que ejecuta la consulta los mismos permisos que tiene el propietario de la consulta.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-104">In a multiuser environment with a secure workgroup, use this declaration with a query to give the user who runs the query the same permissions as the query's owner.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cfd9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6cfd9-105">Syntax</span></span>

<span data-ttu-id="6cfd9-106">*instrucciónsql* CON OWNERACCESS OPTION</span><span class="sxs-lookup"><span data-stu-id="6cfd9-106">*sqlstatement* WITH OWNERACCESS OPTION</span></span>

## <a name="remarks"></a><span data-ttu-id="6cfd9-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6cfd9-107">Remarks</span></span>

<span data-ttu-id="6cfd9-108">La declaración WITH OWNERACCESS OPTION es opcional.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-108">The WITH OWNERACCESS OPTION declaration is optional.</span></span>

<span data-ttu-id="6cfd9-109">En el siguiente ejemplo, se permite al usuario ver información de salarios (incluso si el usuario no tiene permiso para ver la tabla de nóminas Payroll), siempre que el propietario de la consulta tenga dicho permiso:</span><span class="sxs-lookup"><span data-stu-id="6cfd9-109">The following example enables the user to view salary information (even if the user does not otherwise have permission to view the Payroll table), provided that the query's owner does have that permission:</span></span>

``` sql
SELECT LastName, 
FirstName, Salary
FROM Employees 
ORDER BY LastName 
WITH OWNERACCESS OPTION;
```

<span data-ttu-id="6cfd9-110">Si de otra manera un usuario tiene prohibido crear una tabla o agregarle datos, puede usar WITH OWNERACCESS OPTION para permitir que el usuario ejecute una consulta de creación de tabla o de datos anexados.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-110">If a user is otherwise prevented from creating or adding to a table, you can use WITH OWNERACCESS OPTION to enable the user to run a make-table or append query.</span></span>

<span data-ttu-id="6cfd9-111">Si desea aplicar la configuración de seguridad de grupo de trabajo y los permisos de los usuarios, no incluya la declaración WITH OWNERACCESS OPTION.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-111">If you want to enforce workgroup security settings and users' permissions, do not include the WITH OWNERACCESS OPTION declaration.</span></span>

<span data-ttu-id="6cfd9-p101">Esta opción requiere que tenga acceso al archivo System.mdw asociado con la base de datos. Sólo es útil en implementaciones multiusuario protegidas.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-p101">This option requires you to have access to the System.mdw file associated with the database. It is useful only in secured multiuser implementations.</span></span>

