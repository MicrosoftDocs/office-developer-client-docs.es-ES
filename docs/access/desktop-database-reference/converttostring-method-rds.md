---
title: ConvertToString (método, RDS)
TOCTitle: ConvertToString Method (RDS)
ms:assetid: dc6381e4-98c8-badc-ad8c-87c70574a8a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250113(v=office.15)
ms:contentKeyID: 48548136
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7483144ff3ab9b93ae35bdebff951c5b4415786c
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860514"
---
# <a name="converttostring-method-rds"></a><span data-ttu-id="fa430-102">ConvertToString (método, RDS)</span><span class="sxs-lookup"><span data-stu-id="fa430-102">ConvertToString Method (RDS)</span></span>


<span data-ttu-id="fa430-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa430-103">**Applies to**: Access 2013 | Office 2013</span></span> 

<span data-ttu-id="fa430-104">Convierte un objeto [Recordset](recordset-object-ado.md) en una cadena MIME que representa los datos del conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="fa430-104">Converts a [Recordset](recordset-object-ado.md) to a MIME string that represents the recordset data.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa430-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fa430-105">Syntax</span></span>

<span data-ttu-id="fa430-106">*DataFactory*. ConvertToString (objeto de*conjunto de registros*)</span><span class="sxs-lookup"><span data-stu-id="fa430-106">*DataFactory*.ConvertToString(*Recordset*)</span></span>

## <a name="parameters"></a><span data-ttu-id="fa430-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fa430-107">Parameters</span></span>

  - <span data-ttu-id="fa430-108">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="fa430-108">*DataFactory*</span></span>

  - <span data-ttu-id="fa430-109">Variable de objeto que representa un objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md).</span><span class="sxs-lookup"><span data-stu-id="fa430-109">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>

  - <span data-ttu-id="fa430-110">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="fa430-110">*Recordset*</span></span>

  - <span data-ttu-id="fa430-111">Variable de objeto que representa un objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="fa430-111">An object variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa430-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fa430-112">Remarks</span></span>

<span data-ttu-id="fa430-113">Con archivos .asp, use **ConvertToString** para incrustar el objeto **Recordset** en una página HTML generada en el servidor para su transmisión a un equipo de cliente.</span><span class="sxs-lookup"><span data-stu-id="fa430-113">With .asp files, use **ConvertToString** to embed the **Recordset** in an HTML page generated on the server to transport it to a client computer.</span></span>

<span data-ttu-id="fa430-114">**ConvertToString** carga primero el objeto **Recordset** en las tablas del servicio de cursor y, a continuación, genera una secuencia en formato MIME.</span><span class="sxs-lookup"><span data-stu-id="fa430-114">**ConvertToString** first loads the **Recordset** into the Cursor Service tables, and then generates a stream in MIME format.</span></span>

<span data-ttu-id="fa430-p101">En el cliente, el Servicio de datos remoto puede volver a convertir la cadena MIME en un objeto **Recordset** de plena funcionalidad. Esto funciona bien cuando se manipulan menos de 400 filas de datos y el ancho de cada fila no supera los 1024 bytes. No debe usarse para transmitir datos BLOB ni conjuntos de resultados de gran tamaño a través de HTTP. No se realiza ningún tipo de compresión en la cadena, por lo que los conjuntos de datos de tamaño muy grande tardarán bastante en transmitirse a través de HTTP en comparación con el formato de tablagrama optimizada que el Servicio de datos remoto define e implementa como su formato de protocolo de transporte nativo.</span><span class="sxs-lookup"><span data-stu-id="fa430-p101">On the client, Remote Data Service can convert the MIME string back into a fully functioning **Recordset**. It works well for handling fewer than 400 rows of data with no more than 1024 bytes width per row. You shouldn't use it for streaming BLOB data and large result sets over HTTP. No wire compression is performed on the string, so very large data sets will take considerable time to transport over HTTP when compared to the wire-optimized tablegram format defined and deployed by Remote Data Service as its native transport protocol format.</span></span>


> [!NOTE]
> <span data-ttu-id="fa430-p102">[!NOTA] Si utiliza páginas Active Server para incrustar la cadena MIME resultante en una página HTML de cliente, tenga en cuenta que las versiones de VBScript anteriores a la versión 2.0 limitan el tamaño de la cadena a 32 K. Si se supera este límite, se devuelve un error. Mantenga el ámbito de consulta bastante reducido al utilizar la incrustación MIME a través de archivos .asp. Para solucionar esto, descargue la última versión de VBScript del [Centro de descarga de Microsoft](https://www.microsoft.com/downloads/en/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="fa430-p102">If you are using Active Server Pages to embed the resulting MIME string in a client HTML page, be aware that versions of VBScript earlier than version 2.0 limit the string's size to 32K. If this limit is exceeded, an error is returned. Keep the query scope relatively small when using MIME embedding via .asp files. To fix this, download the latest version of VBScript from the [Microsoft Download Center](https://www.microsoft.com/downloads/en/default.aspx).</span></span>


