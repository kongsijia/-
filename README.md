# -
取交集
setwd("G:/GTExTCGA_GBM/interset")
diff<-read.table("diff.txt",sep="\t",header=T,check.names=F)
survival<-read.table("survival.txt",sep="\t",header=T,check.names=F)
list<-read.table("list.txt",sep="\t",header=T,check.names=F)
diff_survival<-intersect(diff$gene,survival$gene)
diff_survival_a<-as.data.frame(diff_survival)
diff_survival_list_text<-intersect(diff_survival_a$diff_survival,list$gene)
diff_survival_list<-as.data.frame(diff_survival_list_text)
unique_list<-unique(list)
unique_diff_survival_list<-unique(diff_survival_list)

